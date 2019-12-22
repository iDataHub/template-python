# 数据分析项目模板（Python）
## 0x00 先决条件
- 思想
    - [提问的智慧](https://github.com/tvvocold/How-To-Ask-Questions-The-Smart-Way/)
    - [中文文案排版指北](https://github.com/sparanoid/chinese-copywriting-guidelines/)
    - [标准风格的 README](https://github.com/RichardLitt/standard-readme/)（入门可参照 `minimal-readme.md` ）
- 工具
    - [Python 3.7 文档](https://docs.python.org/3.7/)（或者其他版本）
    - [Pipenv：Python 开发工作流程](https://github.com/pypa/pipenv/)（或者其他虚拟环境）
    - [GitHub 帮助文档](https://docs.github.com/en/github/)（或者其他 Git 服务器）
- 规范
    - [PEP 8：Python 代码风格指南](https://www.python.org/dev/peps/pep-0008/)
    - [架构整洁之道](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)（可选）


## 0x01 项目初始化
1. 使用本项目作为模板：
    - 打开[仓库模板](../../)，点击 <a class="btn btn-sm btn-primary ml-2" href="../../generate">Use this template</a> 从仓库创建模板。
2. 为项目选择合适的 `LICENSE`：
    - 参考[为仓库添加许可](https://docs.github.com/en/github/building-a-strong-community/adding-a-license-to-a-repository/)，如果不熟悉可默认选择 [MIT License](https://opensource.org/licenses/MIT/).
3. 不要上传无意义文件，将其文件名添加至 [`.gitignore`](https://docs.github.com/en/github/using-git/ignoring-files) 文件中：
    - 隐私数据（服务器配置信息、密码等）；
    - 中间文件（神经网络训练模型、生成或下载的测试数据等）；
    - 大文件（25 MB 以上，可以使用网盘存储并赋上链接）。
4. 在上传示例数据时，确保进行[数据脱敏](https://wiki.mbalib.com/wiki/数据脱敏)。
5. 参照前文编写 `README.md`，简要概况项目信息，如果项目历时较长，可以编写 `CHANGELOG`（变更日志）。


## 0x02 项目结构
```sh
$ tree -F --dirsfirst
.
├── article/
├── code/
├── data/
├── temp/
├── LICENSE
├── Pipfile
└── README.md

4 directories, 3 files
```

最初的项目结构包括 4 个文件夹：`article`（文章）、`code`（代码）、`data`（数据）及 `temp`（临时），包含 3 个文件：`LICENSE`（许可）、`Pipfile`（依赖控制）、`README.md`（自述文件）。

其中四个文件夹的作用见其字面意思。值得一提的是，所有的数据文件放置在 `data` 文件夹下，运行程序时想要获取数据则需经常使用 `..`，因此可以在 `code` 文件夹下使用配置文件存储数据路径，防止硬编码（`os.path.join`）。

`LICENSE` 在前文已经创建，以后除非更改许可外，不需对其进行操作。`README.md` 为自述文件，如果需要不同版本的自述文件，建议新建类似 `README.en.md` 的不同语言自述文件。`Pipfile` 则是 Pipenv 进行依赖管理时生成的，在运行程序时建议进入虚拟环境，语法等请参照前文。

隐藏文件包括 `.git/` 与 `.gitignore`，前者为记录版本控制的文件夹，无需进行更改。后者则记录 push 时忽略的文件，语法等请参照前文。


## 0x03 问题反馈
本模板针对数据分析项目制定，欢迎于 [Issues](../../issues) 页面进行问题反馈。
