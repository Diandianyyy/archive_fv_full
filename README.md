# FV 全版本源自动备份

上游：https://kiIIuaaa.github.io/repo/

备份越狱源：https://diandianyyy.github.io/archive_fv_full/

GitHub Actions 每 6 小时检查更新（北京时间 02:17、08:17、14:17、20:17；调度可能延迟），也可手动运行。

只运行一个同步任务，请求至少间隔 3 秒。对比 SHA-256，仅下载未备份的安装包，校验大小、哈希和 DEB 格式。遇到 429 或暂时性错误按响应要求等待重试。默认每轮最多下载 100 个包；手动运行时输入 `max_downloads=0` 可全部补齐，每 100 个包提交一次。

同步提交由 `github-actions[bot]` 使用 Actions 自带的临时令牌完成，不需要个人 PAT。Pages 发布索引，安装包地址指向本仓库的固定提交。上游删除旧版本时仍保留已归档的包；不备份上游的全部 Git 历史。
