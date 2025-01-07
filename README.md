## 简介 

[![Join Discussions](https://img.shields.io/github/discussions/oucailab/OUC-LaTex-bachelor)](https://github.com/oucailab/OUC-LaTex-bachelor/discussions)

🔥🔥🔥 特别提示，之前本仓库链接在：https://github.com/summitgao/OUC-LaTex-bachelor 因为启用了2FA验证密码无法找回，现在启用本仓库继续维护。欢迎有问题在[讨论区](https://github.com/oucailab/OUC-LaTex-bachelor/discussions)发帖讨论

本模板是中国海洋大学本科生毕业论文LaTeX模板。LaTeX是一个流行的编辑科学类文章的工具。 大多数科学类书籍，期刊，文章都采用了LaTeX。 使用这个模板可以使你从无聊的格式限制中解脱出来，从而更专注地阐述自己的想法。 希望本模板能够帮助你入门LaTeX, 如果你有关于本模板的良好意见和建议，请在顶栏的问题(Discussions)进行讨论。

学习LaTeX可以参考 Overleaf 的官方教程（[Learn LaTeX in 30 minutes](https://cn.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes)），或者在B站学习碗豆老师的45分钟教学视频 “[Latex科研写作入门](https://www.bilibili.com/video/BV1Au411N7Ew/)”。

本模板已经帮助2017级以来的多届中国海洋大学本科毕业生使用，在学生及答辩专家中反馈良好，大家可以放心使用。

有任何问题可以联系： gaofeng@ouc.edu.cn

<br>

## 1. 如何使用？

### 1.1 Overleaf

**本模板在 Overleaf 下测试通过。** 可以通过链接：<https://cn.overleaf.com/read/ymrxysrnchhm>   在线浏览本项目。

![img](img/20210422170337.jpg)

Overleaf 是一个线上 LaTeX 编辑器，可以在不安装任何工具的情况下编写 LaTeX 文档，同时也可以和其他人共享文档，共同编辑。

推荐使用 **Overleaf** 使用本模板，具体方法如下：

1. 下载模板代码，并压缩成 .zip 文件
2. 在 Overleaf 中上传这个 .zip 压缩文件以创建一个新 Overleaf 项目
3. 在 Overleaf 界面左上角点击 "Menu"
   - 选择 "Compiler" 为 "XeLaTeX"
   - 选择 "TeX Live version" 为 "2019" 或者更新的版本
4. 使用 Overleaf 编译

### 1.2 Overleaf

推荐大家使用 [TexPage](https://www.texpage.com/)，可以理解为国产版的 Overleaf，对于国内用户支持的要好一些，尤其是云盘同步功能，支持百度网盘和 WebDAV 。另外，遇到问题客服也很给力，发邮件能够12小时以内及时回复帮忙解决问题，大家可以考虑。点击下面图标可以直接打开 TexPage 中的模板。

[![TeXPage](https://img.shields.io/badge/OUC-TeXPage-495A80.svg)](https://www.texpage.com/template/fce6f583-3a96-4494-8d59-8bd4deb45c5d)

<br>

### 1.2 本地编译

本项目在Windows下测试通过，理论上支持所有系统，本地编译测试使用的版本为TeX Live 2021。无论使用哪一个编辑器或IDE，都**需要使用XeLaTeX而不是默认的pdfLaTeX**。第一部分是安装LaTeX环境，必选，其余部分是编辑器或IDE，可选。

#### 本地安装LaTeX环境(必选)

推荐使用TeX Live，下载及安装可参照[The Not So Short Introduction To LaTeX2ε (Chinese Edition)](https://github.com/CTeX-org/lshort-zh-cn)中的**附录 A 安装 TEX 发行版**，国内推荐使用镜像源。

```url
https://mirrors.ustc.edu.cn/CTAN/systems/texlive/Images/
https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/Images/
```

安装过程花费半小时属于正常现象，耐心等待即可。

#### Tex Live自带编辑器TeXworks

使用自带编辑器TeXworks时，左上角更改为**XeLaTeX**即可使用。但是自带编辑器功能简陋，年久失修，一般建议使用其他编辑器。

![img](img/image-20220305144537228.jpg)

#### VS Code + LateX Workshop

如题所示，需要安装**LateX Workshop**插件，效果图如图所示。

本项目已经自带.vscode/setting.json配置文件，所以可以直接构建，点击左侧TEX中的build或者右上角的绿色构建按钮都可。如果希望VSCode默认使用XeLaTeX，而不局限于本项目，请将.vscode/setting.json中的内容添加到你的VSCode本身的setting中，这样就不需要每个工作区重新配置XeLaTeX了。

![img](img/image-20220305143913352.jpg)

#### IntelliJ IDEA + TeXiFy IDEA

如题所示，但不局限于IDEA，只要是JetBrains出品的IDE都可，譬如下图使用的就是PyCharm，添加**TeXiFy IDEA**插件即可使用，如果要在IDE内部直接浏览生成的PDF，还需要安装**PDF Viewer**插件。

编译需要先找到tex文件中的**\\begin\{document\}**，点击其左侧的运行按钮，第一次会运行失败，然后编辑上方的**配置**，将编译器改为**XeLaTeX**即可。
或者直接**"文件->新项目设置->运行配置模板->LaTeX->编译器"**改为**XeLaTeX**，这样新项目默认都是使用XeLaTeX。

![img](img/image-20220305144343929.jpg)

#### TeXstudio

TeXstudio上述均是全平台的，此编辑器仅限Windows平台。需要将**选项->设置TeXstudio->构建->默认编译器**改为XeLaTeX。

![img](img/image-20220305143708631.jpg)

#### 文本编辑器

如果使用系统自带文本编辑器的话，需要在命令行中编译PDF。

```shell
xelatex -file-line-error -interaction=nonstopmode -synctex=1 main.tex
```

### 1.3 注意事项

可能需要编译两次才可以正确显示目录

## 2. 反馈与贡献

本模版是由诸多感兴趣的同学一起维护的开源项目，我们非常欢迎问题反馈和新的贡献者！

### 2.1 反馈问题

如果在使用上有任何问题，建议通过以下方式进行反馈（按推荐顺序排序）：

* 如遇不会使用、编译错误等问题，请至 [在 GitHub 项目讨论区提问](https://github.com/oucailab/OUC-LaTex-bachelor/discussions) (推荐)
* 如遇模版 BUG，或有新的需求，请至 [在 GitHub 项目中提 issue](https://github.com/oucailab/OUC-LaTex-bachelor/issues)



### 成为贡献者

这个仓库是面向用户的**示例模版**，如果你有很好的排版示例，可以提交到此仓库与大家分享。如果你想为本仓库贡献代码，欢迎发 Pull Request，然后再将更新同步到本仓库。

除了提交 Pull Request 之外，还有以下方式可以进行贡献：

* 帮助我们解答同学们的[问题](https://github.com/oucailab/OUC-LaTex-bachelor/discussions)，这些问题你也可能遇到过并且知道如何解决；
* 向周围同学安利 OUC-LaTex-bachelor，让更多的同学使用我们维护的模板；
* 在讨论区中分享你的使用体验，以及吐槽。如果你也想成为项目的长期维护者，也可以通过邮件/讨论区告诉我们。:-)



## 开源许可

本项目代码基于 MIT 协议开源

学校标志的版权归中国海洋大学所有
