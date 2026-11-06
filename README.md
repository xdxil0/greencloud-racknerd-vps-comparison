# greencloud vs racknerd：低价 VPS 到底选哪家？价格、配置、退款风险与亚洲机房一次说清

搜 greencloud vs racknerd 的人，纠结点其实就三个：同样一年几十美元，谁的硬件更值；面向亚洲用户的流量谁跑得顺；万一不合适能不能退。先把结论放在前面：

- **只想花最少的钱开一台 Linux 小机**：RackNerd 的年付特价更便宜，1GB 配置 $21.99/年，且官方 FAQ 明确特价套餐终身同价续费。
- **在意 CPU 和磁盘性能、需要 10Gbps 端口或亚洲机房**：GreenCloud 的规格更高，官网 Budget KVM 产品线全线 10Gbps 上联，主力节点为 EPYC 处理器加 NVMe RAID-10（部分过季节点为 Xeon E5v4 + SSD）。
- **需要 Windows VPS、习惯支付宝付款**：GreenCloud 的 Windows 线 $8/月起且包含授权，付款支持支付宝、银联和加密货币。

> **选购速览**：GreenCloud 预算线最省事的选择是 SSDKVM-1（$6/月，1 核 1GB / 15GB SSD / 1.5TB 流量 / 10Gbps）；打算长期用，可以看年付的 Budget KVM 促销系列（第三方整理价约 2GB 档 $25/年起，历史促销价、以结算页实时价格为准，售完即止）。注意：该系列不退款。👉 [查看 GreenCloud Budget KVM 当前套餐与库存](https://greencloudvps.com/billing/aff.php?aff=6679)

## 两家的定位差别在哪

这两家虽然都出现在“便宜 VPS”的搜索结果里，但打法完全不同。

RackNerd 的核心是年付特价：1GB KVM 特价 $21.99/年（1 核 / 20GB SSD / 3TB 流量），2GB $35.99/年（2 核 / 35GB / 5TB），4GB $59.99/年，最高 8GB 档 $119.99/年。它的常规 KVM 线以 Intel Xeon 为主，另有 Ryzen 线，端口 1Gbps，数据中心约 20 个，北美为主，洛杉矶节点是亚洲优化线路。

GreenCloud 走的是“低价但硬件不缩水”的路线：官网 Budget KVM 产品线全线 10Gbps 端口，主力节点用 EPYC Rome/Milan 加 NVMe RAID-10，官方标称 99.99% SLA、工单平均响应 9 分钟。机房覆盖三大洲超过 17 个位置，亚洲有东京（分 IIJ 线和 Softbank 线）、新加坡（DC1 为 EPYC、另有 DC2）、香港，以及河内和胡志明市——这点 RackNerd 没有对等布局，它的亚洲覆盖主要靠洛杉矶优化线路。

简单说：拼绝对低价，RackNerd 赢；拼同价位下的硬件规格和亚洲网络，GreenCloud 赢。

## GreenCloud 全套餐价格表

GreenCloud 当前官网公开的套餐分四条线：Budget KVM（Linux，月付）、Budget KVM 促销系列（年付）、Budget Windows VPS（月付）和 Windows SuperSaving（季度起付折扣）。需要大容量存储的话它还有一条 Storage KVM VPS 线，可按 $5/TB/月加购至 20TB 硬盘，适合做备份仓的用户。

### Budget KVM VPS（Linux，月付，全线 10Gbps）

| 套餐 | CPU / 内存 | SSD 存储 | 月流量 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- |
| SSDKVM-1 | 1 核 / 1GB | 15GB | 1.5TB（亚太 750GB） | $6/月 | [ 购买 SSDKVM-1](https://greencloudvps.com/billing/aff.php?aff=6679) |
| SSDKVM-2 | 1 核 / 2GB | 15GB | 2TB（亚太 1TB） | $10/月 | [ 购买 SSDKVM-2](https://greencloudvps.com/billing/aff.php?aff=6679) |
| SSDKVM-3 | 2 核 / 4GB | 30GB | 4TB（亚太 2TB） | $20/月 | [ 购买 SSDKVM-3](https://greencloudvps.com/billing/aff.php?aff=6679) |
| SSDKVM-4 | 4 核 / 8GB | 60GB | 8TB（亚太 4TB） | $40/月 | [ 购买 SSDKVM-4](https://greencloudvps.com/billing/aff.php?aff=6679) |
| SSDKVM-5 | 8 核 / 16GB | 120GB | 12TB（亚太 6TB） | $80/月 | [ 购买 SSDKVM-5](https://greencloudvps.com/billing/aff.php?aff=6679) |

亚太机房（新加坡、东京、香港等）的流量配额是欧美机房的一半左右，这是很多人在下单后才发现的事，下单前就要算进去。

### Budget KVM 促销系列（年付，售完即止）

这档按机房分货销售，第三方整理的规格大致是三档：2GB 档（1 核 / 20GB NVMe / 2TB 流量）约 $25/年，4GB 档（2 核 / 35GB / 4TB 流量）约 $30/年，8GB 档（4 核 / 60GB / 8TB 流量）约 $45/年。这些都是历史促销整理价，同配置不同机房价格可能不同，实际以结算页显示为准。全部套餐含 1 个 IPv4、IPv6、10Gbps 端口和 1 次免费备份/快照。

一个多数对比文章没提的现状：截至最近一次页面核验，这档促销的 NVMe + EPYC 节点（纽约、阿什本、洛杉矶、圣何塞、凤凰城、阿姆斯特丹、多伦多等）已全部售罄，**有货的只剩芝加哥 DC2、杰克逊维尔和堪萨斯城三个位置，且全部是 SSD 存储 + Xeon E5v4 老一代硬件**。冲着"EPYC + NVMe"四个字下单的话，先确认机房，不然拿到手的可能只是 E5v4 + SSD。顺带一提，堪萨斯城的 IPv6 只有 /112，其他机房是 /64，对 IPv6 有要求的注意避开。另外这档按机房下单后不能切换，换机房等于重新下单。

### Budget Windows VPS（Windows Server 2022，1Gbps，不限流量，月付）

| 套餐 | CPU / 内存 | SSD 存储 | 价格 | 购买 |
| --- | --- | --- | --- | --- |
| US1 | 1 核 / 1GB | 25GB | $8/月 | [ 购买 US1](https://greencloudvps.com/billing/aff.php?aff=6679) |
| US1.5 | 1 核 / 1.5GB | 30GB | $12/月 | [ 购买 US1.5](https://greencloudvps.com/billing/aff.php?aff=6679) |
| US2 | 2 核 / 2GB | 40GB | $16/月 | [ 购买 US2](https://greencloudvps.com/billing/aff.php?aff=6679) |
| US3 | 2 核 / 3GB | 60GB | $24/月 | [ 购买 US3](https://greencloudvps.com/billing/aff.php?aff=6679) |
| US4 | 4 核 / 4GB | 80GB | $32/月 | [ 购买 US4](https://greencloudvps.com/billing/aff.php?aff=6679) |
| US5 | 5 核 / 5GB | 100GB | $40/月 | [ 购买 US5](https://greencloudvps.com/billing/aff.php?aff=6679) |
| US6 | 6 核 / 6GB | 120GB | $48/月 | [ 购买 US6](https://greencloudvps.com/billing/aff.php?aff=6679) |

Windows 授权包含在价格里。官方明确允许 Hitleap/Jingling 这类流量交换工具，同类服务商大多禁止这个用途，有相关需求的可以直接认准这一条。需要 2GB 内存的话，看下面 SuperSaving 线更划算。

### Windows SuperSaving（季度起付享折扣）

| 套餐 | CPU / 内存 | SSD 存储 | 价格 |
| --- | --- | --- | --- |
| Budget-1 | 1 核 / 2GB | 25GB | $10/月 |
| Budget-2 | 2 核 / 4GB | 40GB | $20/月 |
| Budget-3 | 4 核 / 8GB | 80GB | $40/月 |

SuperSaving 比 Normal 系列内存多一倍，代价是至少按季度付费，且属于特殊折扣方案（退款政策见下文）。

## 核心参数对比：GreenCloud vs RackNerd

| 项目 | GreenCloud | RackNerd |
| --- | --- | --- |
| 入门年付价 | Budget KVM 促销 2GB 档约 $25/年（历史价，视库存） | 1GB 特价 $21.99/年，3TB 流量 |
| 常规入门 | SSDKVM-1 $6/月（1 核 1GB / 10Gbps） | 512MB $26.99/年；1GB $17.99/月 |
| 端口 | Budget KVM 全线 10Gbps | 1Gbps |
| 存储 | NVMe / SSD RAID-10，按机房而定 | SSD RAID-10 |
| 机房 | 三大洲 17+ 位置，亚洲有东京/新加坡/香港 | 约 20 个数据中心，北美为主，洛杉矶亚洲优化 |
| CPU 型号 | 公开（EPYC Rome/Milan 或 E5v4，按机房） | 特价款未公布 |
| 退款 | 7 天，限新客户首台；促销款不退款 | 特价款通常适用标准退款政策（标准线为 30 天），以官方页面为准 |

## 价格背后的真实账

单看年费，RackNerd 更便宜：1GB 特价 $21.99/年，折合每月不到 $2，而且官方 FAQ 写明这类特价套餐是 lifetime recurring，续费同价。GreenCloud 同样预算买不到月付机——它的低价年付入口主要就是 Budget KVM 促销系列，2GB 档约 $25/年已经是起步价，而且经常缺货。

换到月付线，账就反过来了。GreenCloud SSDKVM-1 是 $6/月、1GB 内存、10Gbps 端口；RackNerd 常规线 1GB 是 $17.99/月。RackNerd 的月付线定价明显偏高，它的低价逻辑是把你锁进年付。所以：确定要跑一年以上、预算卡死 → RackNerd 年付；想要灵活性或更高规格 → GreenCloud 月付反而是更合理的选择。

## 退款政策和下单前的三个注意点

这是 greencloud vs racknerd 对比里最容易被略过、又最容易踩坑的部分。

1. **GreenCloud 的 7 天退款有范围限制**。退款只针对新客户的首台 VPS，且“特别折扣套餐除外”——Budget KVM 促销系列每个套餐都直接标注 No refund/Money back。也就是说，你冲着 $25/年 下的单，付款那一刻起就没有反悔通道。
2. **RackNerd 的退款相对宽松**。标准 KVM 线有 30 天退款保证，特价款通常也适用标准退款政策（以购买页当时展示的条款为准）。想先低成本试水再决定的人，这一点足以影响选择。
3. **两家都是 unmanaged**。GreenCloud 官方写明只负责物理服务器和在线率，软件问题不协助处理；RackNerd 同样是自管型 VPS。没有 Linux 基础的话，别指望工单帮你装环境。

使用限制上也各有各的红线。RackNerd 条款明确：KVM VPS 内跑虚拟机、hypervisor 属于嵌套虚拟化，需书面批准且不保证 VT-x/AMD-V 可用（Docker、LXC、Kubernetes 等容器负载明确允许）；加密货币挖矿、邮件群发一律禁止。GreenCloud 这边，Budget KVM 仅限 Linux 系统。

另外 GreenCloud 有反欺诈审核：账单信息不准确（比如 IP 地区对不上）会延迟开通。付款方式倒是齐全，PayPal、信用卡、支付宝、银联、BTC/ETH/USDT 等加密货币都支持，新客户用信用卡或 PayPal 首次付款需要一次性验证。开通时间一般 15 分钟内，最长约 2 小时；RackNerd 是即时交付，30 分钟没收到开通邮件先查垃圾箱。

## 亚洲机房和流量：差距最明显的一块

面向东亚和东南亚用户的服务，GreenCloud 的优势是实打实的：东京节点分 IIJ 和 Softbank 两条优化线路，另有新加坡、香港，以及少见的河内、胡志明市节点。RackNerd 的亚洲覆盖依赖洛杉矶优化线路，亚洲方向绕行在所难免。

不过有一条第三方测评的观察值得记下：GreenCloud 的亚洲线路白天延迟表现不错，但晚高峰丢包率偏高，回程没有 CN2 GIA 级别的深度优化，更适合白天使用或对晚高峰不敏感的场景。代价还有流量减半：SSDKVM-1 在欧美有 1.5TB/月，亚太只有 750GB；年付促销款在新加坡直接降到 750GB–1.5TB。跑视频代理或大流量下载的话，这个差距要先算清楚。

👉 [查看 GreenCloud 各机房当前库存与流量配额](https://greencloudvps.com/billing/aff.php?aff=6679)

## 谁不适合选 GreenCloud

坦白讲，有三类人可以不用考虑它。预算压到极限、一年只想花二十来美元的，RackNerd 特价款价格低一档还带退款保护；所在地区只有欧美机房有货时，GreenCloud 现在能买的促销款全是 E5v4 + SSD 的老硬件，规格卖点无从谈起；需要 30 天无理由退款兜底的，7 天新客户首台的条款太紧。

## FAQ

**GreenCloud 能用支付宝付款吗？** 能。支持 PayPal、信用卡/借记卡、支付宝、银联、加密货币（BTC/ETH/BNB/USDT 等）以及美英欧银行转账。

**Budget KVM 后续能加配置吗？** 可以。RAM $3/GB/月、CPU $3/核/月、SSD $3/10GB/月，最多加到原配置的一倍，且取决于服务器资源可用性。要海量存储则建议看它的 Storage KVM VPS 线，$5/TB/月起。

**开通要等多久？** GreenCloud 付款后一般 15 分钟内开通，个别情况最长 2 小时；账单信息与实际不符会触发反欺诈延迟。RackNerd 为即时交付。

**RackNerd 特价款续费会涨价吗？** 不会。其官方 FAQ 明确特价套餐终身同价续费（lifetime recurring）。

**GreenCloud 的 99.99% SLA 可信吗？** 这是官网自述口径，配合公开状态页，没有独立的第三方验证，参考即可。

## 怎么选，最后一句话

跑北美或欧洲流量、预算优先、想留退款后路 → RackNerd 年付特价。跑亚洲流量、要 EPYC + NVMe 规格、需要 Windows 或支付宝付款 → GreenCloud。有用户干脆两家各买一台：RackNerd 洛杉矶扛北美流量，GreenCloud 新加坡扛亚洲流量，分工比单押一家更稳。

下单 GreenCloud 之前确认两件事：所选机房当前有货、且你接受它的硬件代际（EPYC/NVMe 还是 E5v4/SSD）；你买的这个套餐是不是“特殊折扣方案”，如果是，7 天退款条款对它不适用。确认完就可以👉 [前往 GreenCloud 按机房开通](https://greencloudvps.com/billing/aff.php?aff=6679)。
