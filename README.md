# 免费代理节点订阅

自动收割 → 去重 → 测速筛选后的可用节点，**每 2 小时更新**。

## 订阅地址

| 用途 | 地址 |
|---|---|
| base64 订阅（推荐） | `https://raw.githubusercontent.com/12ccl/proxypool-nodes/main/sub.txt` |
| 明文节点列表 | `https://raw.githubusercontent.com/12ccl/proxypool-nodes/main/nodes.txt` |
| 按协议 | 见下方「文件说明」 |

> Clash / Mihomo / v2rayN / Shadowrocket / sing-box 都能直接导入 `sub.txt`。

## 在线工具

**订阅转换工具**（纯前端，数据不出浏览器，支持 Clash / Mihomo / sing-box 转换、加分流规则、重命名节点）：

| 入口 | 地址 | 说明 |
|---|---|---|
| 主入口 | `https://clash-sub-converter-19641.app.workbuddy.host/?sharecode=AETYY3P2LK` | 国内可直连 |
| GitHub Pages | `https://12ccl.github.io/proxypool-nodes/` | 需要能访问 github.io |

> `github.io` 在国内多数网络下无法访问（DNS 污染），优先用主入口。
> 也可以直接下载仓库里的 `index.html` 用浏览器打开，纯离线可用。

## 当前数据

| 项目 | 数值 |
|---|---|
| 更新时间 | 2026-11-01 20:42:35 +0800 |
| 可用节点 | **3** |
| 本轮测试 | 524 个候选 → 3 个达标 |
| 数据来源 | GitHub 搜索 `v2ray free` 前 675 个仓库 |

## 筛选标准

1. TCP 连通 + HTTP 测活通过（`gstatic.com/generate_204`）
2. 下载速度 ≥ **1 MB/s**，低于这个值直接丢弃
3. 按「服务器:端口」去重（同一台机器的多个协议只留一个）
4. 按历史稳定度排序，连续通过的排在最前面

## 协议分布

| 协议 | 数量 |
|---|---|
| vless | 1 |
| trojan | 1 |
| vmess | 1 |

## 稳定性

| 连续通过轮数 | 节点数 |
|---|---|
| ≥ 3 轮 | 3 |
| 2 轮 | 0 |

> 这些节点来自互联网公开的公益分享，**原始存活率约 0.1%**。
> 本仓库只保留通过测速的那部分，但仍然随时可能失效。

## 文件说明

| 文件 | 说明 |
|---|---|
| `nodes.txt` | 全部节点，一行一个 URI（超过 8MB 自动分片为 `nodes-001.txt` …） |
| `<协议>.txt` | 按协议拆分（同样会分片） |
| `sub.txt` | base64 编码的订阅文件（节点过多时不生成） |

## 更新机制

- **每小时**：重新收割 GitHub 上的公开节点源
- **每 2 小时**：去重 → 测活 → 测速 → 更新本仓库
- 连续失败 3 次的节点不再进入测试队列，省下的时间用来测新节点

## 免责声明

- 所有节点均来自互联网公开仓库，本仓库仅做自动汇总与可用性筛选。
- 不保证任何节点的可用性、稳定性或安全性，请自行判断使用风险。
- 请遵守所在地区的法律法规。

## 节点数最多的来源文件

| 仓库 | 文件 | 节点数 |
|---|---|---|
| 3000S-HTTP/sNSub | `output/configs_vless_vmess.txt` | 24,079 |
| Nexuspt753/GitHub-Sub-Scanner | `subs/all.b64.txt` | 20,359 |
| myominn062-svg/mk-studio-vpn-service | `subscription-trojan.txt` | 18,412 |
| M-Mashreghi/Free-V2ray-Collector | `All_Configs_Sub.txt` | 16,637 |
| M-Mashreghi/Free-V2ray-Collector | `All_shuffled_config.txt` | 16,637 |
| Nexuspt753/GitHub-Sub-Scanner | `subs/all.txt` | 15,943 |
| funykaly/V2ray-Configs-Tester | `configs/all_scraped.txt` | 15,800 |
| Twitr/Free-V2ray-Collector | `All_Configs_Sub.txt` | 15,701 |
| myominn062-svg/mk-studio-vpn-service | `subscription-ss.txt` | 15,474 |
| longlon/v2ray-config | `All_Configs_base64_Sub.txt` | 13,165 |
