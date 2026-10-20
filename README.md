# ofd-fixtures

本仓库存放 [`zc310/ofd`](https://github.com/zc310/ofd) 测试使用的 OFD/PDF 样例，
避免样例增加主代码仓库的体积，并保留测试所需的目录结构和文件名。

## 目录结构

```text
testdata/
  ofd-creator/   创建器生成的常规和大页数 OFD 样例
  ofdrw/         与 ofdrw 相关的第三方 OFD 样例
  pdf2ofd/       PDF 转 OFD 的回归样例
  libofd/        libofd 来源 PDF 样例
  pdfcpu/        pdfcpu 来源 PDF 样例
  standards/     标准文档 PDF 样例
  suwell/        Suwell 来源 PDF 样例
  tencent/       腾讯 PDF 样例
  apple/         Apple PDF 样例
  google/        Google PDF 样例
  microsoft/     Microsoft PDF 样例
```

新增样例时，优先保留上游文件名和原始内容，并按来源项目归档。请记录样例的上游地址、
许可和必要的署名信息。仓库根目录的 `LICENSE` 不替代第三方文档自身的许可及署名要求。

## 在 ofd 中使用

在 `ofd` 仓库目录运行以下命令：

```sh
make fixtures
```

该目标从 GitHub 下载 `main` 分支压缩包，并将其中整个 `testdata/` 目录复制到 `ofd`
仓库的对应目录。可通过 Make 变量 `FIXTURES_URL` 指定其他分支、标签或提交对应的压缩包
地址。运行该目标需要安装 `curl` 和 `unzip`。
