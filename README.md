<div align="center">
  <a href="#"><img src="https://kiramibot.dev/img/logo.svg" width="180" height="180" alt="KiramiBotPluginLogo"></a>
</div>

<div align="center">

# kirami-plugin-example

_✨ KiramiBot 插件简单描述 ✨_


<a href="./LICENSE">
    <img src="https://img.shields.io/github/license/owner/kirami-plugin-example.svg" alt="license">
</a>
<a href="https://pypi.python.org/pypi/kiramibot-plugin-example">
    <img src="https://img.shields.io/pypi/v/kirami-plugin-example.svg" alt="pypi">
</a>
<img src="https://img.shields.io/badge/python-3.10+-blue.svg" alt="python">

</div>

这是一个 KiramiBot 插件项目的模板库, 你可以直接使用本模板创建你的 KiramiBot 插件项目的仓库

模板库使用方法:
1. 点击仓库中的 "Use this template" 按钮, 输入仓库名与描述, 点击 "Create repository from template" 创建仓库
2. 在创建好的新仓库中, 在 "Add file" 菜单中选择 "Create new file", 在新文件名处输入`LICENSE`, 此时在右侧会出现一个 "Choose a license template" 按钮, 点击此按钮选择开源协议模板, 然后在最下方提交新文件到主分支
3. 全局替换`owner`为仓库所有者ID; 全局替换`kirami-plugin-example`为插件名; 全局替换`kirami_plugin_example`为包名; 修改 python 徽标中的版本为你插件的运行所需版本
4. 修改 README 中的插件名和插件描述, 并在下方填充相应的内容

配置发布工作流:
1. 跟随 [PyPI 文档](https://docs.pypi.org/trusted-publishers/) 配置 可信发布
   - **PyPI Project Name** 插件名，如：`kirami-plugin-xxx`
   - **Owner** 你的 Github 用户名
   - **Repository name** 仓库名，如：`kirami-plugin-xxx`
   - **Workflow name** 发布工作流，填写 `release.yml`
   - **Environment name** 是你的发布环境，填写 `release`
     
   例如，如果您有一个位于 https://github.com/octo-org/sampleproject 的存储库，其发布工作流程位于 `release.yml`，并且您希望将其作为示例项目发布到 PyPI，那么您将执行以下操作： 
   <div align="left">
     <img src="https://docs.pypi.org/assets/pending-publisher-form-filled.png" style="wight: 1000px; height: 600px"/>
   </div>

3. 进入工作流，修改 `environment`
   
   ```yaml
   environment:
      name: release
      url: https://pypi.org/p/<your-pypi-project-name>
   ```

4. 发版


## 📖 介绍

这里是插件的详细介绍部分

## 💿 安装

在 KiramiBot 项目的插件目录下, 打开命令行, 根据你使用的包管理器, 输入相应的安装命令

<details>
<summary>pip</summary>
  
```bash
pip install kirami-plugin-example
```
</details>
<details>
<summary>pdm</summary>

```bash
pdm add kirami-plugin-example
```
</details>
<details>
<summary>poetry</summary>

```bash
poetry add kirami-plugin-example
```
</details>
<details>
<summary>conda</summary>

```bash
conda install kirami-plugin-example
```
</details>

打开 KiramiBot 项目根目录下的配置文件, 以 `kirami.toml` 为例，在 `[plugin]` 部分追加写入
```toml
plugins = ["kiramit_plugin_example"]
```

## ⚙️ 配置

在 KiramiBot 项目的配置文件中添加下表中的必填配置

| 配置项 | 必填 | 默认值 | 说明 |
|:-----:|:----:|:----:|:----:|
| 配置项1 | 是 | 无 | 配置说明 |
| 配置项2 | 否 | 无 | 配置说明 |

## 🎉 使用
### 指令表
| 指令 | 权限 | 需要@ | 范围 | 说明 |
|:-----:|:----:|:----:|:----:|:----:|
| 指令1 | 主人 | 否 | 私聊 | 指令说明 |
| 指令2 | 群员 | 是 | 群聊 | 指令说明 |
### 效果图
如果有效果图的话
