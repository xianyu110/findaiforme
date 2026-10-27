# 中国独立开发者 · AI 新站（镜像区）

本目录是 [chinese-independent-developer](https://github.com/xianyu110/chinese-independent-developer)（上游聚合：[@1c7/chinese-independent-developer](https://github.com/1c7/chinese-independent-developer)）中 **AI 相关** 站点的 FindAIForMe 侧镜像。

| | |
|---|---|
| 主站「最新 AI」 | https://findaifor.me/ （首页 Tab） |
| 本仓库（主 hub） | https://github.com/xianyu110/findaiforme |
| 上游独立开发者列表 | https://github.com/xianyu110/chinese-independent-developer |
| 同步脚本 | AIToolsDir `scripts/sync-indie-developer.mjs` |

## 关系说明

- **findaiforme 为主**：AI 工具目录与站点展示以本仓库 + findaifor.me 为准。
- **chinese-independent-developer 为上游信源**：每日新站仍由该列表维护；本目录只收 **AI 相关**、已上线、可访问的网站，并按 URL/slug 去重后写入 findaifor.me。
- **不删除也不取代** 原独立开发者全量列表（含非 AI / 游戏 / 程序员版面）。

## 最近同步

见 [`AI-RECENT.md`](./AI-RECENT.md)。标签 `chinese-independent-developer` / `CN Indie` 标记来源。

更新命令（在 AIToolsDir 仓库）：

```bash
node scripts/sync-indie-developer.mjs --days 3
npx wrangler d1 execute melodygift-db --remote --file=scripts/sql-batches/indie-sync.sql -y
node scripts/build-edge-snapshots.mjs
npm run deploy
```
