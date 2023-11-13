# Vue I18n Extractor

Vue I18n Extractor 是一个用于 Vue.js 项目的命令行工具，它可以帮助你自动化国际化(i18n)的过程。这个工具会自动抽取 Vue 组件模板中的中文文本和属性，并将其替换为函数包裹的格式。此外，它还会根据提取出的中文文本，自动生成一个翻译配置文件，这个文件可以用于更方便的引用，也可以用来提交翻译。

## 安装 Installation

你可以通过 npm 来安装 Vue I18n Extractor：

You can install Vue I18n Extractor via npm:

```bash
npm install vue-i18n-extractor
```

## 使用 Usage

你可以通过命令行参数来使用 Vue I18n Extractor。以下是一些可用的参数：

- `-f` 或 `--file`：指定要处理的单个文件的路径。
- `-d` 或 `--directory`：指定要处理的目录的路径。默认为当前目录。
- `-e` 或 `--exclude`：指定要排除的目录。这应该是一个目录的数组。

例如，以下命令会处理当前目录及其子目录中的所有文件，但不会处理 `./doc` 和 `./txt` 目录：

In this example, the tool will process the file at ./src/pages/index.vue and will exclude ./src/pages/exclude.vue.

```bash
vue-i18n-extractor -d ./ -e ./doc -e ./txt
```

## 功能

Vue I18n Extractor 主要有以下功能：

1. **自动抽取中文文本和属性**：Vue I18n Extractor 会遍历你的 Vue 组件模板，找到所有的中文文本和属性，并将其替换为函数包裹的格式。

2. **生成翻译配置文件**：Vue I18n Extractor 会根据抽取出的中文文本，自动生成一个翻译配置文件。这个文件可以用于更方便的引用，也可以用来提交翻译。

3. **支持单个文件和目录**：你可以指定要处理的单个文件，也可以指定要处理的目录。如果指定了目录，Vue I18n Extractor 会递归处理该目录下的所有文件。

4. **支持排除目录**：你可以指定要排除的目录。Vue I18n Extractor 不会处理这些目录下的文件。

The tool generates a translation configuration file or a text file containing all the extracted Chinese text. This file can be used for further translation work.

## 注意事项

Vue I18n Extractor 仅支持 Vue 组件模板中的中文文本和属性。它不会处理其他类型的文件，也不会处理 Vue 组件模板以外的中文文本和属性。