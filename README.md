# mindmap-models

[MindMap](https://github.com/wuyunyoujiduo-jpg/mindmap) 的可选插件，供应用按需下载。这里只有模型文件，没有代码。

## embed/ — 资料库语义检索

离线的向量模型，让资料库按意思搜索、推荐相关资料。

- 来源：[minishlab/potion-multilingual-128M](https://huggingface.co/minishlab/potion-multilingual-128M)（Model2Vec，由 BAAI/bge-m3 蒸馏；许可以原模型页面为准）
- 处理：保留中文、日文、英文的常用词元，向量按行量化为 int8，约 23MB
- 分成 15MB 的小块，以便通过 jsDelivr 镜像下载；`manifest.json` 记录每块和整体的 SHA-256，应用下载后逐一校验

生成方法见 MindMap 仓库的 `tools/embedmodel`。
