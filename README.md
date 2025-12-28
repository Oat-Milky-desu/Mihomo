# Mihomo Configuration

这是一个 Mihomo (Meta) 代理配置仓库，包含自动同步规则文件的 GitHub Action。

## 功能

- **自动同步规则**：每天自动从远程仓库下载最新的规则文件到 `rules/` 文件夹
- **手动触发**：支持在 GitHub Actions 页面手动触发同步

## 文件说明

| 文件 | 说明 |
|------|------|
| `config.yaml` | Mihomo 主配置文件 |
| `rules.json` | 规则 URL 配置文件 |
| `rules/` | 下载的规则文件存放目录 |

## 使用方法

### 添加/修改规则

编辑 `rules.json` 文件，在 `rules` 数组中添加新条目：

```json
{
  "name": "规则名称",
  "format": "文件格式(如 mrs 或 yaml)",
  "url": "规则文件的下载地址"
}
```

### 手动触发同步

1. 进入仓库的 **Actions** 页面
2. 选择 **Sync Rule Providers** 工作流
3. 点击 **Run workflow** 按钮

### 定时同步

工作流每天 **08:00（北京时间）** 自动执行，无需手动操作。

## 许可证

MIT
