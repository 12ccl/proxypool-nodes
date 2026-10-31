# proxypool-nodes

从 GitHub 公开仓库收割的代理节点清单，自动生成。

- 生成时间：2026-10-31 15:36:43 +0800
- 节点总数：**71**（已去重）
- 来源仓库：见 `harvest_report.csv` 的统计

## 协议分布

| 协议 | 数量 |
|---|---|
| vless | 35 |
| trojan | 15 |
| ss | 13 |
| hysteria2 | 7 |
| vmess | 1 |

## 文件说明

| 文件 | 说明 |
|---|---|
| `nodes.txt` | 全部节点，一行一个 URI（超过 8MB 会自动分片为 `nodes-001.txt` …） |
| `<协议>.txt` | 按协议拆分（同样会分片） |
| `sub.txt` | base64 编码的订阅文件（节点过多时不生成） |

## 直接当订阅用

```
https://raw.githubusercontent.com/12ccl/proxypool-nodes/main/sub.txt
```

## 注意

- 这些是**公开收集**的免费节点，存活率很低（实测 5% 左右），随时可能失效。
- 节点凭据来自公开仓库，请自行判断使用风险。
- 本仓库只做汇总，不保证可用性。

## 节点数最多的来源文件

| 仓库 | 文件 | 节点数 |
|---|---|---|
| 3000S-HTTP/sNSub | `output/configs_vless_vmess.txt` | 24,287 |
| Nexuspt753/GitHub-Sub-Scanner | `subs/all.b64.txt` | 20,359 |
| twj0/subseek | `data/sub_github_base64.txt` | 19,271 |
| twj0/subseek | `data/sub_github.txt` | 19,271 |
| myominn062-svg/mk-studio-vpn-service | `subscription-trojan.txt` | 17,572 |
| M-Mashreghi/Free-V2ray-Collector | `All_Configs_Sub.txt` | 16,637 |
| M-Mashreghi/Free-V2ray-Collector | `All_shuffled_config.txt` | 16,637 |
| Nexuspt753/GitHub-Sub-Scanner | `subs/all.txt` | 16,429 |
| funykaly/V2ray-Configs-Tester | `configs/all_scraped.txt` | 15,800 |
| Twitr/Free-V2ray-Collector | `All_Configs_Sub.txt` | 15,701 |
