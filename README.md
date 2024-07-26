<div align="center">
  <a href="#"><img src="https://kiramibot.dev/img/logo.svg" width="180" height="180" alt="KiramiBotPluginLogo"></a>
</div>

<div align="center">

# kirami-plugin-fishing

_✨ 根据星露谷物语图片素材，粗制滥造的群内钓鱼小游戏 ✨_


<a href="./LICENSE">
    <img src="https://img.shields.io/github/license/owner/kirami-plugin-fishing.svg" alt="license">
</a>
<a href="https://pypi.python.org/pypi/kirami-plugin-fishing">
    <img src="https://img.shields.io/pypi/v/kirami-plugin-fishing.svg" alt="pypi">
</a>
<img src="https://img.shields.io/badge/python-3.10+-blue.svg" alt="python">

</div>


## 📖 介绍

素材采自 [星露谷物语Wiki](https://stardewvalleywiki.com/Stardew_Valley_Wiki)，群内钓鱼娱乐小游戏，**提前刷屏警告**。

## 💿 安装

在 KiramiBot 项目的插件目录下, 打开命令行, 根据你使用的包管理器, 输入相应的安装命令

<details>
<summary>pip</summary>
  
```bash
pip install kirami-plugin-fishing
```
</details>
<details>
<summary>pdm</summary>

```bash
pdm add kirami-plugin-fishing
```
</details>
<details>
<summary>poetry</summary>

```bash
poetry add kirami-plugin-fishing
```
</details>
<details>
<summary>conda</summary>

```bash
conda install kirami-plugin-fishing
```
</details>

打开 KiramiBot 项目根目录下的配置文件, 以 `kirami.toml` 为例，在 `[plugin]` 部分追加写入
```toml
plugins = ["kiramit_plugin_fishing"]
```

## ⚙️ 配置

在 KiramiBot 项目的配置文件中添加下表中的必填配置

|         配置项         | 必填 |   默认值    |       说明        |
|:-------------------:|:--:|:--------:|:---------------:|
|    fishing_limit    | 否  |   1800   |  钓鱼CD时间（单位：秒）   |
|   fish_multiplier   | 否  |   1.0    |   获取积分（鱼干）倍率    |
| fishing_time_radius | 否  | [30,150] | 上钩时间[最小时间,最大时间] |
|  fishing_coin_name  | 否  |   块小鱼干   |     钓鱼积分名称      |
|  fish_empty_chance  | 否  |   0.1    |      空军概率       |

## 🎉 使用
### 指令表
|   指令    | 权限 | 需要@ | 范围 |       说明        |
|:-------:|:--:|:---:|:--:|:---------------:|
|  钓鱼/🎣  | 群员 |  否  | 群聊 |       钓鱼        |
|  钓鱼统计   | 群员 |  否  | 群聊 |  获取个人群内钓鱼统计信息   |
|  钓鱼排名   | 群员 |  否  | 群聊 | 获取群内钓鱼排行榜（按最重鱼） |
| 钓鱼余额/鱼干 | 群员 |  否  | 群聊 |  获取群内钓鱼积分排行统计   |
| 钓鱼手册/鱼鉴 | 群员 |  否  | 群聊 |    获取钓鱼收集图鉴     |

### 自定义鱼类
**1、添加json数据**

插件会在启动时，补全json数据到kirami的数据目录下的`fishing`文件夹下，在该文件内新增鱼类数据和稀有度即可。
鱼类数据添加到对应稀有度下，格式如下：
```json
{
  "legendary": {
      "BlueShark": {
        "display-name": "鱼名",
        "weight-min": 160, //  最小重量
        "weight-max": 240,  //  最大重量
        "msg": "捕获特殊文字"
      }
  }
}
```
**2、添加图片（可选）**

插件启动时，会检测kirami资源图片目录下是否有`fish`文件夹，如果没有，则自动创建，并下载默认图包。
如果需要添加自定义鱼类的图片，只需要将该以json文件中，与展示名称相同的文件名的图片放入该目录即可。

### 资源下载

如果插件启动时，无法下载资源，请手动下载资源。

[默认鱼类图片包](https://raw.githubusercontent.com/FrostN0v0/kirami-plugin-fishing/master/resources/fish.zip)，解压后，将解压后的文件夹放入kirami的资源图片目录`resources/image/fish`下。

[图鉴字体](https://raw.githubusercontent.com/FrostN0v0/kirami-plugin-fishing/master/resources/Uranus_Pixel_11Px.ttf]

[数据json文件](https://raw.githubusercontent.com/FrostN0v0/kirami-plugin-fishing/master/resources/fishes.json)

### 效果图
<img align="left" src="https://ghproxy.com/https://raw.githubusercontent.com/FrostN0v0/kirami-plugin-fishing/master/resources/example1.jpg" width='380px' alt="钓鱼示例">

<img align="left" src="https://ghproxy.com/https://raw.githubusercontent.com/FrostN0v0/kirami-plugin-fishing/master/resources/example2.jpg" width='380px' alt="钓鱼手册示例">
