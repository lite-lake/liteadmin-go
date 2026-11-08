# 更新日志

本项目的公开版本历史。日期为发布日；条目面向使用者视角，不涉及内部过程。

## [v0.1.0] - 2026-11-09

### 新增
- 开源首个公开发布：Admin 委托认证协议包，供管理平台侧与上游服务共同引用，保证协议两端零漂移。
- `X-Lite-Admin-*` 协议头常量与 Id 格式校验（全仓头名唯一权威），`crypto/subtle` 常数时间密钥比较。
- `DelegatedIdentity` 轻量委托身份结构与 `NewDelegatedSession` 字段助手，Session 实体由接入服务回调映射。
- `UpstreamClient` 上游委托调用客户端：注入委托头与链路追踪头，默认 15 秒超时。
- `GenerateKey` 密钥生成（32 字节密码学安全随机数 → base64url，多把并存支持轮换）与 `cmd/keygen` 批量生成命令行工具。
