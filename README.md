# dsh-desk

DeepSeek Harness Desktop 的更新源（nightly feed）。

## 结构

```
<release-id>/
  feeds/
    mac-arm64/
      nightly-mac.yml     # electron-updater 清单
```

安装包本体不放在本仓库（GitHub 单文件上限 100 MB），由清单里的绝对 URL 指向
本仓库的 [Releases](../../releases) 资产。

## 为什么有 release-id

上游把测试发布批次 ID 编进更新 URL。已安装的客户端会把清单地址烧死，
因此**后续所有版本必须沿用同一个 ID**，否则老客户端永远收不到更新。

当前在用：`679f6328098b8130de67b803f69559ab`

## 上游

源代码来自 [deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness)（MIT）。
本仓库只承载更新清单，不含源码改动。
