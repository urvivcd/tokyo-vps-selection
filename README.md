# tokyo vps：东京机房怎么选，线路、价格、退款条款一篇讲清楚

搜 tokyo vps 的人基本分两类：一类要给中国用户低延迟出口，盯着回程线路；另一类要在东亚放业务节点（API、游戏服、面板），更关心稳定性和总成本。这两类人的最优解差别很大，而市面上大部分东京 VPS 文章把所有套餐混在一起谈，没说清差别在哪。

先给结论：V.PS（vps.hosting，xTom 旗下品牌）在东京有两条不同的产品线——Cloud KVM VPS（SoftBank 线路，€6.95/月起）和 Performance KVM VPS（AMD EPYC Gen 2 机型、CN2 GIA 线路，€49.95/月起），另有每年 €39.95 的 Mini KVM。多数轻度用户选 €6.95 那档就够了；跑生产业务、对回程有硬需求的，再看 EPYC 系列。

> **选购速览**
> - 个人项目、开发测试 → 东京 SoftBank 的 Cloud KVM，2核1G/20GB SSD/1TB 流量，€6.95/月
> - 要 EPYC 算力 + NVMe + CN2 GIA 回程 → Performance KVM 的 Tokyo EPYC Flash Gen 2，2核4G/30GB NVMe/1TB，€49.95/月
> - VPS 产品 14 个自然日内可退款（有例外条款）；99.9% SLA；每个套餐含 1 IPv4 + 1 IPv6
> - 👉 [查看 V.PS 东京套餐当前价格](https://vps.hosting/products/cart/cloud-kvm-vps/?affid=1666)

## V.PS 东京产品线：两条网络，定位差 7 倍

东京市场里“便宜”和“中国优化”是两个独立变量，V.PS 把这点做得很直白——它家东京有两条网络，各有独立的 looking glass，买之前能测到自己所购套餐的真实路由。

| 产品线 | 线路 | 存储 | 起价 | 适合 |
| --- | --- | --- | --- | --- |
| Cloud KVM（东京 SoftBank） | SoftBank，三网直连 | SSD | €6.95/月 | 个人项目、开发测试 |
| Performance KVM（东京 EPYC Gen 2） | CN2 GIA | NVMe | €49.95/月 | 生产业务、中国方向 |
| Mini KVM | 与 Cloud 共用东京网络 | — | €39.95/年 | 极轻量用途 |

关于线路质量，第三方测评的说法可以参考：东京 SoftBank 线路去程和回程都走 Softbank（bbtec/BBIX），电信和联通延迟低，移动稍高一些；EPYC Gen 2 系列则明确走 CN2 GIA。xTom 本身做了十多年 IP transit，很多下游主机商的软银线路就是从他家买的——这也是 V.PS 网络底子的来源。

## 全套餐对比：东京 8 款 + 大阪 4 款

日本区共 12 款 VPS 套餐在售，全部有货。东京 SoftBank 四档的具体配置来自两家独立第三方在售页交叉核对，与官网 €6.95 起价一致；EPYC 四档配置与官网下单页完全对应。

**Cloud KVM VPS（东京 SoftBank）—— SSD 存储、1TB 流量、1 Gbps：**

| 套餐 | 配置 | 价格（月付） | 购买 |
| --- | --- | --- | --- |
| 2核1G | 2 核 / 1GB / 20GB SSD | €6.95 | [ 开通东京 SoftBank 入门款](https://vps.hosting/products/cart/cloud-kvm-vps/?affid=1666) |
| 2核2G | 2 核 / 2GB / 30GB SSD | €7.95 | [ 开通东京 SoftBank 2核2G](https://vps.hosting/products/cart/cloud-kvm-vps/?affid=1666) |
| 4核4G | 4 核 / 4GB / 40GB SSD | €9.95 | [ 开通东京 SoftBank 4核4G](https://vps.hosting/products/cart/cloud-kvm-vps/?affid=1666) |
| 8核8G | 8 核 / 8GB / 80GB SSD | €19.95 | [ 开通东京 SoftBank 8核8G](https://vps.hosting/products/cart/cloud-kvm-vps/?affid=1666) |

**Performance KVM VPS（东京 EPYC Gen 2，CN2 GIA）—— AMD EPYC + NVMe：**

| 套餐 | 配置 | 网络 | 购买 |
| --- | --- | --- | --- |
| EPYC Flash Gen 2 | 2核 / 4GB / 30GB NVMe / 1TB 流量 | 1 Gbps | [ 查看东京 EPYC Flash 当前价](https://vps.hosting/?action=add&cmd=cart&id=259&affid=1666) |
| EPYC Flow Gen 2 | 2核 / 8GB / 60GB NVMe / 2TB 流量 | 1.25 Gbps | [ 查看东京 EPYC Flow 当前价](https://vps.hosting/?action=add&cmd=cart&id=259&affid=1666) |
| EPYC Fleet Gen 2 | 4核 / 16GB / 120GB NVMe / 4TB 流量 | 2 Gbps | [ 查看东京 EPYC Fleet 当前价](https://vps.hosting/?action=add&cmd=cart&id=259&affid=1666) |
| EPYC Formula Gen 2 | 8核 / 32GB / 240GB NVMe / 8TB 流量 | 2.5 Gbps | [ 查看东京 EPYC Formula 当前价](https://vps.hosting/?action=add&cmd=cart&id=259&affid=1666) |

**大阪 IIJ 四档**：配置结构与东京 SoftBank 完全一致（2核1G €6.95 → 8核8G €19.95，SSD、1TB 流量、1Gbps），走 IIJ 线路直连，就不单独列表了——要的只是“日本有台机器”的话，大阪和东京差别不大。

官网还展示几条非东京产品线，列出备查：Edge KVM VPS、Storage KVM VPS（文件服务器用）、Shared cPanel Hosting（小型企业虚拟主机）、SSL 证书（GoGetSSL 提供，DV 和 Wildcard）。全部入口见 👉 [V.PS 官网产品页](https://vps.hosting/products/?affid=1666)。

价格口径三点：全部欧元计价，标价之外另计 VAT（结账按账户所在地计算）；下单时可切换计费周期，第三方信息称年付可减免约 2 个月费用，以结账页实际显示为准；有比价站评价 V.PS“价格表长期稳定”，不用担心到手价和宣传价对不上。

## 买之前先测路由：两个 looking glass

V.PS 东京的两条网络各配了独立 looking glass，官网东京页提供入口，支持 ping、traceroute 和测速。Performance KVM 对应 premium 网络那条，Cloud 和 Mini 共用另一条。第三方资料还给出了东京测试 IP（103.201.131.131），可以直接从本地测到机器的真实表现。

这个动作建议别跳过，尤其是冲着 CN2 GIA 去的读者——€49.95/月起的套餐，路由是否符合预期值得花两分钟确认，14 天退款条款用不上最好，但前提是你下单前就该心里有数。

## EPYC 系列的隐藏成本：设置费和 IPv6 加购

Performance KVM 的标价之外，还有几项只写在 FAQ 和下单细节里的费用，很多文章不会提：

- **月付有额外设置费，季付及以上免设置费**。也就是说 EPYC 系列按月买反而多花钱，打算长期用就直接选季付起步。
- **默认含 1 个 IPv4 和 1 个 IPv6**；如果需要 /48 的 IPv6 段，要额外付费（第三方资料口径为 €9.00/月 + €15.00 一次性设置费）。一般用户用不上这个段，知道有这回事就行。
- **流量可以加购，最高可调至 100TB/月**。Cloud 系列默认 1TB，不够同样可以加购。

CPU 是 AMD EPYC 7763，DDR4 内存加 NVMe SSD，资源是保证型而非共享型——这也是它和低价档拉开差价的核心：€49.95 买的算力和 €6.95 买的算力，在超售策略上完全不同。

## 退款、注册注意事项与支持

**退款**：VPS 产品支持 14 个自然日内退款，有例外条款，完整条件在官方 FAQ。这个期限比常见的“新账户 30 天退款”短，但比只给 3 天甚至不退的服务商宽松。14 天够你跑完 looking glass 测试、用真实业务流量压几天，不合适就退。

**注册**：有一条很实际的提醒来自第三方测评——注册时不要开代理，资料乱填会导致订单无法开通。填真实信息，一次过。

**支持**：分三档。所有客户都有免费的 24x7 Developer Support，官方原话是 "Open a ticket and a person who runs this network answers"——工单由运营这张网络的人直接回复，不是外包客服。企业客户另有 Business Support 和保证响应时间的付费 Premier Support。

**IP 售后**：新购机器发现 IP 有问题，开工单可以找客服更换；自己弄坏的 IP 更换需要 3 美元。对做建站和 outbound 业务的人，这个细节挺关键。

## 横向对比：同价位东京 VPS 都给什么

以下竞品数据来自第三方比价与测评（未逐一到各官网核验，以各家官网为准），取入门档配置：

| 服务商 | 入门配置 | 价格 | 备注 |
| --- | --- | --- | --- |
| **V.PS** | 2核1G / 20GB SSD / 1TB 流量 / 1Gbps | €6.95 | SoftBank 三网直连，14 天退款 |
| ExtraVM | 1GB RAM 起 | $4.50/mo | 东京 KVM NVMe，DDoS 防护 |
| ByteVirt | 1核512M / 8GB NVMe / 500GB 流量 | $16.88/yr（年付） | 三网直连但非优化（电信 163、移动 CMI、联通 4837） |
| Virtono | 1 vCPU / 1GB / 30GB SSD / 1TB | €4.50 | 东京节点，比价站 11 月初核对 |
| 搬瓦工 The Tokyo Plan v2 | 2核 / 2GB / 40GB SSD / 1TB 流量 / 5Gbps | $99/yr（年付） | 三网 CMI 直连，限量套餐 |

三点观察：

1. 纯比价格，V.PS 排不进最便宜一档，但 €6.95 给到 2 核、1Gbps 端口和 SoftBank 线路，同价位多数产品还在 1 核/512M 档。
2. 中国优化是另一个价位段。搬瓦工限量 Tokyo Plan v2 年付 $99（折合约 €93/月），V.PS 的 CN2 GIA 从 €49.95/月起。两条路都成立：预算足、要稳定供应选 V.PS；抢得到限量套餐且年付预算敏感的，搬瓦工那个价格确实难找对手。
3. ByteVirt 走的是借 DMIT 机房卖低价 CN2 的路线，适合预算极紧的个人用户；但全线 CPU 是共享型，和 EPYC 保证型资源放一起比纯性能不合适。

还有个容易被忽略的点：V.PS 每个套餐标配 1 IPv4 + 1 IPv6，不少低价 VPS 的 IPv4 要按月加租。需要给服务绑独立 IP 的话，这是隐性省钱项。

## 购买与部署流程

官网下单页的口号是 "Setup your server within minutes"，实际就三步：

1. **创建账户**。邮箱注册，注意前面说的：真实资料、别开代理。
2. **选套餐和位置，结账**。这一步可以切换计费周期；选 EPYC 系列的话，直接季付起步避开设置费。
3. **上线**。官方描述 "No tickets, no waiting"，下单后数秒到几分钟开通，不用等人工审核。

装系统支持 Debian Stable、Ubuntu LTS、CentOS Stream、Rocky Linux、AlmaLinux，其他发行版走 netboot.xyz ISO 自装。开服后重启、重建、扩容都在 client area 面板完成，也有 API 可以脚本化管理——要把 VPS 纳入自动化流程的话，这点比纯网页面板实用。

## 按场景选：最后一步

- **个人开发、学习、自托管小服务** → 东京 SoftBank 的 2核1G（€6.95/月），不够再升 2G（€7.95）
- **要内存和算力、跑数据库或编译任务** → SoftBank 的 8核8G（€19.95/月），或 EPYC Flow（8GB NVMe 机型）
- **要 EPYC 算力 + CN2 GIA 回程，业务对网络敏感** → EPYC Flash Gen 2（€49.95/月），季付起步，👉 [先看 EPYC 系列当前配置和价格](https://vps.hosting/?action=add&cmd=cart&id=259&affid=1666)
- **极轻量、年付预算制** → Mini KVM（€39.95/年），与 Cloud 共用东京网络
- **不在乎在日本哪里** → 大阪 IIJ 入门款，同价同配置

下单前最后确认两件事：一看 looking glass 测的路由是否达到预期，二把 14 天退款条款的例外情形读一遍。都确认了就 👉 [去 V.PS 挑一款东京套餐部署](https://vps.hosting/products/cart/cloud-kvm-vps/?affid=1666)，几分钟后你的服务器就在 NTT East Komagome 的机架里跑起来了。
