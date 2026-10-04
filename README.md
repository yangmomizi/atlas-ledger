# Atlas Ledger Pro V2

## 核心定位
本地优先的个人资本管理终端，而非普通记账 App。

## V2 新增
- 业绩页面：TWR、MWR/XIRR 近似、QQQ+SPY 基准、Alpha、最大回撤、波动率、Sharpe、Sortino
- 风险页面：资产集中度、账户暴露、基础风险检查
- 导入页面：CSV / JSON 基础流水导入
- 数据页面：完整 JSON 备份、交易 CSV 导出
- 截图 OCR 入口（当前为 OCR 接口预留；未把图片上传第三方）
- 本地优先：核心账本使用 localStorage
- PWA：manifest + service worker
- iOS 安全区与移动端交互优化

## 重要说明
V2 是可运行的前端产品原型。行情接口和 OCR 仍然建议在下一阶段换成稳定的生产级数据源/本地或自建代理。
收益率模块已经有 TWR / 回撤 / 风险指标框架，但如果要作为严肃投资绩效系统，应进一步使用每日 NAV 快照和精确资金流时间戳计算真正的 TWR 与 XIRR。

## iPhone 安装
推荐：
1. 把整个文件夹部署到 HTTPS 静态站点；
2. iPhone Safari 打开 index.html；
3. 分享 → 添加到主屏幕；
4. 从主屏幕启动 Atlas Pro。

如果仅在“文件”App 中打开 index.html，本地账本仍可操作，但 PWA、Service Worker、部分联网接口可能受到 iOS 文件协议限制。

## 数据安全
不要把 localStorage 当作唯一备份。使用「数据 → 导出账本 JSON」定期备份。
