基于 [heartleo/image-copy](https://github.com/heartleo/image-copy)。

## 使用

1. 仓库 **Settings → Secrets** 配置 `REGISTRY`、`REGISTRY_USERNAME`、`REGISTRY_PASSWORD`、`REGISTRY_NAMESPACE`
2. 编辑 `images.yaml` 填入要复制的镜像，提交到 `main` 自动触发

```yaml
images:
  - src: redis:7-alpine
  - src: postgres:16-alpine
```

| 字段 | 必填 | 说明 |
|------|------|------|
| `src` | 是 | 源镜像 |
| `dest` | 否 | 目标镜像，省略则自动推导为 `REGISTRY/NAMESPACE/<镜像名>` |
| `multi_arch` | 否 | `true` 复制全部架构 |

## License

MIT
