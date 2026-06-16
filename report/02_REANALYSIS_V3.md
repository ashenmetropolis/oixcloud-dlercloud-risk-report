# 02 oixCloud 问题反馈重新分析 v3

## 一、这份新文件的价值

新文件共 203 页，明显比上一份反馈窗口更完整。它不仅包含文字反馈，还包含大量截图，覆盖：

- Shadowrocket；
- FlClash / FIClash for oixCloud；
- Quantumult X / QX；
- Surge；
- OpenClash；
- Clash Verge；
- Loon / Stash / Karing；
- Windows / macOS / iOS / Android / 路由器。

这说明问题不是单一用户、单一客户端、单一平台造成。

## 二、核心问题类型

### 1. Unauthorized / 鉴权异常

反馈中反复出现“Unauthorized / UNAUTHORITY / 未授权”。常见场景包括：

- 更新客户端后无法登录；
- 添加配置时报 Unauthorized；
- Windows/macOS 客户端登录失败；
- 官方 FlClash 重启后丢配置、重新登录；
- 老版本可用，新版本不可用。

代表片段：

- uli9n969s / 更新后，打开提示“unauthorized”, 如何解决。 / Jre4eJv
- flclash / 显示unauthorized是怎么回事，正在用突然就不行了 / a1I5nv3
- uli9n969s / 更新后，打开提示“unauthorized”, 如何解决。 / 更新后
- eyonhnCT / 更新了最新的客户端，重新添加配置文件，报错Unauthorized. / soe
- 端最近 / 即便下了FCLASH FOR OIXCLOUD，还是总提示UNAUTHORITY，这是什么原因？ / COMA
- 端最近 / 即便下了FCLASH FOR OIXCLOUD，还是总提示UNAUTHORITY，这是什么原因？ / 退出账号 重新登录
- oixcloud / 后，登录显示unauthorized。是什么原因 / ooosssol
- 我的windows安装后提示这个 / unauthorized / ，总0518开始就这样了

判断：这不是普通节点慢，而是账号、订阅、客户端、鉴权体系稳定性问题。

### 2. 订阅/配置/导入失败

集中出现：

- Shadowrocket 订阅失败；
- Surge invalid profile；
- QX / Quantumult X response invalid；
- OpenClash 无法订阅；
- Clash Verge 配置失败；
- 自定义订阅无法使用，只能托管。

代表片段：

- Jre4eJv / 都用不了吗，我也是Windows clash用不起，也增加不了配置。 / 我window for clash 节点都没有了，昨天还有time out ，今天连time out 都看不到了
- oixcloud / ，更新后profile没了，输入URL也不能上网，报add。profile exception：unau… / 我现在是window for clash 和FI Clash for
- o3l6620e / 如何将代理导入使用Clash Verge / kjhg_cbe8
- openclash / 无法订阅 / User_a5deca
- Clrea / surge V5版本不能订阅现在的配置，导入都不行 / Zrbe
- Zrbe / 目前是不是订阅出问题了 / k27ra7m
- qx / 导入报错 / 0nzee009rh
- apple tv 怎么办 / 我目前手机上可以用 loon ，但同一个配置同步到 / atv

判断：这说明开放客户端和第三方客户端体系可用性明显下降。

### 3. 协议兼容与官方端绑定

典型错误包括：

- `proxy 0: snell version error: 4`
- `unsupport proxy type: anytls`
- `obfs mode error: anytls`
- FlClash for oixCloud 可用但第三方端不可用
- 路由器 OpenClash 无法使用

判断：协议变化、封端/官方端依赖、第三方兼容下降是本批证据的核心风险点。

### 4. 节点全红 / Timeout / 少节点

文件中多次出现节点全红、全部 Timeout、节点减少、只有部分线路可用、香港/IEPL/Fusion 可用性差等反馈。

判断：实际可用性并不稳定，且不只是“某个地区个别节点”。

### 5. 工单/客服/售后不足

代表片段：

- 管理员您好 #9331 / 号工单 / 已经两个工作日没有回复了  辛苦您看一下
- uli9n969s / 有客服在吗？  已经提交问题了，紧急联系下 谢谢 / dotau
- uli9n969s / 有客服在吗？ 已经提交问题了，紧急联系下 谢谢 / 感谢，已解决。非常感谢。
- j88wws8 / 怎么联系客服 / anre0g
- 5agYa1g1ynn0 / 你们都可以了吗？我下载了FI  clash 还是没用，下载了检测工具和邀请码，还是不行啊。客服也没回复，快一周了 / UHZ
- 5agYa1g1ynn0 / 你们都可以了吗？我下载了FI clash 还是没用，下载了检测工具和邀请码，还是不行啊。客服也没回复，快一周了 / FlClash

判断：服务故障不是最严重的点，严重的是故障后缺少有效反馈通道，用户只能在窗口互相求助。

### 6. 流量统计异常

这是新文件中最强的新增证据之一。出现：

- 睡醒已经消耗 366G；
- 一晚跑 600G；
- 一个上午跑 2.16T；
- 昨天 100G，今天 1.83T；
- 高速额度突然耗尽；
- 关闭代理/重置参数仍异常。

代表片段：

- 淘宝 / app总是使用代理流量，咋整呢 / eeztirrh
- Harikis / 流量消耗异常，重置参数无用 / euxonx
- euxonx / 流量消耗异常。昨晚还有剩余177G，今早告诉我说已经超限了。查看流量日志，皆为正常流量。请解释怎么回事。 / vo
- 🪜 / 也在消耗流量 / 😕
- Harikis / 流量消耗异常，重置参数无用 / 我也是流量消耗异常
- 流量消耗异常，重置参数无用 / 我也是流量消耗异常 / iltnf
- lhesaneo / 流量统计有问题，我刚睡醒，现在是上午十点，统计今天流量已经使用366G，问题是今天什么都还不没干，人刚醒，昨天就感觉异常，什么都没干 / 一
- 天使用50多G， / 流量统计有问题+1 / 6666_2dcf
- v818_1aa5 / 流量统计有问题还是偷跑了？昨天一天用的流量顶我之前半个月用的 / 6666_2dcf
- v818_1aa5 / 流量统计有问题还是偷跑了？昨天一天用的流量顶我之前半个月用的 / 查查“今天使用”，你会有惊喜

判断：这不是“体验差”层面的风险，而是套餐剩余价值、后台计量可信度和自动续费/限速风险。

### 7. 套餐权益争议

代表片段：

- 撤吧 / 朋友们，刚刚随便找了个30包月的都能用！绝对跑路了，还买的699，还好就剩一个月 / 我还有半年呢？ 到今年10月中旬到期
- sharpzq / 请问一个套餐可以在几个设备同时使用？ / nduuemlP
- 导入Universal链接，连通性测试，只有非常少，不到10%节点可用 / 套餐支持IEPL，电脑端可用，但是手机端不行 / j88wws8
- euxije / 你好，购买套餐后，怎么使用 / shunghzsa
- shunghzsa / 为啥Premium 套餐用不了Premium节点，命名是不是有问题，那不是变相的调低套餐了 / ejwiieah
- shunghzsa / 为啥Premium 套餐用不了Premium节点，命名是不是有问题，那不是变相的调低套餐了 / 基本上是
- 基本上是 / 续费前一些 / 节点名称，续费后一些节点名称。随意修改用户协议。完全不把老用户当人看的。
- 续费前一些 / 节点名称，续费后一些节点名称。随意修改用户协议。完全不把老用户当人看的。 / scNsasuri

涉及：

- 699 套餐未稳定使用；
- Premium 节点使用争议；
- Bronze 原有 IEPL 后期变 Fusion；
- 节点减少；
- 高价套餐用户要求方案/退款；
- 自动续费取消需求。

判断：高价/长期套餐风险进一步坐实。

## 三、对原证据链的加强

新版反馈窗口把原有证据链从：

```text
公告 + 群聊讨论
```

加强为：

```text
公告 + 群聊讨论 + 故障截图 + 用户反馈窗口
```

它能直接证明：用户不是在空口抱怨，而是在集中提交可见错误、截图、工单和异常现象。

## 四、风险等级

| 风险项 | 等级 | 理由 |
|---|---|---|
| 官方端/鉴权风险 | 极高 | Unauthorized 贯穿多平台 |
| 第三方客户端兼容风险 | 极高 | Shadowrocket/QX/Surge/OpenClash/Clash Verge 均有反馈 |
| 稳定性风险 | 高 | 节点全红、Timeout、掉线、少节点 |
| 流量统计风险 | 极高 | 多用户反馈非正常大额消耗 |
| 售后响应风险 | 高 | 工单多日无回复、客服缺位 |
| 高价套餐风险 | 高 | Premium/Bronze/699/长期套餐权益争议 |
| 直接跑路风险 | 中 | 有跑路讨论，但仍有维护和反馈窗口，不能写死 |
| 接盘/换壳/权益缩水风险 | 高 | DlerCloud 延续 + oixCloud 接手后收紧 |

## 五、最终判断

新版文件足以把 oixCloud 从“体验差”升级为：

> 接盘延续盘 + 官方端/鉴权/协议体系不稳定 + 第三方客户端可用性下降 + 流量统计异常 + 高价套餐权益不确定 + 售后响应不足的高风险服务。

最适合公开的结论：

> 不建议新用户购买高价长期套餐；已有用户不建议作为唯一主力；技术用户、路由器用户、第三方客户端用户尤其应谨慎。
