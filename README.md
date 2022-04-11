# zzuthesis

## 根据郑州大学电气工程学院硕士毕业论文要求进行修改：

- 英文字体更改为Times New Roman
- [master分支](https://github.com/gaoyangu/zzuthesis/tree/master)为`专业硕士`版本
- [main分支](https://github.com/gaoyangu/zzuthesis/tree/master)为`学术硕士`版本

### Tips:

Q：如何将章节标题中的英文字体改为Times New Roman

```sh
\textrm{hello}
```

Q：如何去除图目录和表目录中章节之间的空白

1. 找到 `main.lot` 和 `main.lof` 两个文件
2. 使用任意文本编辑器打开
3. 删除其中的 `\addvspace {10.0pt}`
4. 编译**一次**（注意：编译两次后，图目录和表目录将恢复到原来的状态）

---

郑州大学本科毕业设计(论文)和研究生学位论文(含 硕士和博士) LaTeX 模版。 本科毕业设计（论文）和研究生学位论文（含硕士和博士） 分别根据《郑州大学材料科学与工程学院本科毕业设计（论文）基本规范》和《郑州大学学位论文写作规范格式》的规范要求制定。该模板主要完成于 2012 年上半年，在上传至 Github 前进行了部分调整，以保证正常编译运行。

## 1. 字体配置

采用 ctex 宏包中的字体配置。

## 2. 模板编译

该模板分别在 Windows 和 Linux 平台安装的 TeXLive 2019 下测试通过。

### 2.1 模板文件的生成

  `latexmk -xelatex main`

### 2.2 A3 封面文件的生成

  `xelatex spine`
  
  `xelatex a3cover`

### 2.3 自动运行脚本(Makefile)

* `make all`       等于 `make thesis && make a3cover`(默认选项)；
* `make thesis`    生成论文 main.pdf；
* `make a3cover`   生成封面 a3cover.pdf；
* `make clean`     清理中间文件；
