# squid-keepalive

保活探针。每 8 分钟 ping 一次 Render 免费实例的 `/healthz`，
防止它因 15 分钟无流量而休眠、导致企业微信机器人 WebSocket 长连断开。

**本仓库内不含任何业务代码或数据**，目标地址存放在仓库 Secret `BOT_PUSH_URL` 中。

之所以单独拆出来做成 public 仓库：GitHub Actions 对 public 仓库**免费且不限分钟数**，
而私有仓库每月只有 2000 分钟——高频保活会瞬间吃穿额度。
业务仓库 `squid-market` 保持私有不受影响。
