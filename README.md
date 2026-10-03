# 古风猜歌连线游戏

一个蓝白青花瓷古风风格的"猜歌连线"网页小游戏，左右两列歌词卡片连线配对。

## 功能特点

- 🎨 **蓝白青花瓷古风UI**：楷体字体、双层边框卡片、青花瓷背景
- 🎮 **连线玩法**：左右两列歌词卡片连线配对，连对变绿、连错变红
- 🎵 **音频播放**：左右两边都能播放音频切片
- 📊 **数据库存储**：使用 Supabase 存储关卡和歌曲数据
- 👨‍💼 **管理员后台**：支持增删改关卡/歌曲/上传音频切片
- 🎉 **结算动画**：连对撒花动画、古风音效

## 技术栈

- 纯 HTML/CSS/JS 单文件
- Supabase (数据库 + 匿名读写)
- Web Audio API (合成模拟音频)

## Supabase 配置

```javascript
const SUPABASE_URL = 'https://wcxungdjbfeoaonnzudl.supabase.co';
const SUPABASE_KEY = 'sb_publishable_JaR1P8jmca4KwBt9dwVK-Q_-ahKwX2O';
```

### 数据库表结构

**levels 表**
- id (int)
- name (text) - 关卡名称
- particle (text) - 开头词（如"是谁"、"我爱你"）
- sort_order (int) - 排序

**songs 表**
- id (int)
- level_id (int) - 关卡ID
- lyric (text) - 左列歌词
- song (text) - 歌曲名
- left_audio (text) - 左边音频URL
- right_audio (text) - 右边音频URL
- sort_order (int) - 排序

## 游戏说明

1. 打开 `猜歌连线.html` 即可游玩
2. 点击左边歌词卡片，再点击右边对应的歌词卡片进行连线
3. 连对变绿固定连线，连错变红不能修改
4. 一次机会，连错即停止
5. 可以点击"弃权提交"提前结算

## 管理员功能

- 密码：`02468#abAB`
- 支持增删改关卡
- 支持增删改歌曲
- 支持上传左右音频切片

## 歌曲数据

歌词配对大全：`歌词配对大全.xlsx`
- 118首歌词配对
- 10种类型：古风戏腔、是谁开头、我爱你开头、我们开头、你的开头、你是开头、啊开头、如果开头、你说开头、这是开头

## 素材文件

`assets/` 目录包含：
- bg2.jpg - 青花瓷背景图
- hand3.png - 手拿毛笔透明PNG
- 其他装饰素材

## 在线试听链接

部分歌曲已补充QQ音乐链接，可在Excel中查看。
