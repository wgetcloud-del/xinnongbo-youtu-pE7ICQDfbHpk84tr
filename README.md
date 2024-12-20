
大家好，我是汤师爷\~


和退款单作为整个交易逆向系统的核心，支撑着售后管理环节。


### 售后域核心概念模型


![](https://img2024.cnblogs.com/other/2625446/202412/2625446-20241215160755380-1478047433.jpg)


**1、退款单**


退款单是记录和跟踪退款处理过程的核心业务单据，包含以下关键信息：


* 租户ID：标识所属商户或组织
* 退款单ID：退款单的唯一标识
* 原订单ID：关联的原始订单
* 业务类型：仅退款、退货退款等
* 退款类型：如全额退款、部分退款、按商品退款等
* 创建时间：退款单生成的时间
* 退款状态：反映当前售后处理阶段
* 退款原因：记录具体退款原因，如不想要了、商品破损等
* 退款金额：需要退还的具体金额
* 退款手续费：退还的手续费


**2、退款资金信息**


退款资金信息包含了退款处理过程中的关键支付数据，包含以下关键字段：：


* 支付单号：用于关联原支付记录
* 渠道退款单号：支付渠道生成的退款凭证号
* 退款状态：反映当前退款处理的进度，如待处理、处理中、已完成等
* 退款金额：本次需要退还的具体金额数值
* 退款账户：接收退款的目标账户，如用户余额、微信、支付宝等账户。


**3、退款明细**


退款明细记录了每笔退款交易中具体商品的退款信息，包含以下关键字段：


* 退款明细ID：每条退款明细记录的唯一标识
* 商品ID：退款商品的唯一标识
* SKU\_ID：具体的商品规格的唯一标识
* 商品退货数量：本次退回的商品数量
* 商品退款金额：该商品的实际退款金额


### 退款单状态机


**1、仅退款状态机**


仅退款状态机描述了用户申请仅退款时，退款申请单的处理流程和状态转换。核心状态包括待审核、待买家处理、售后完成和售后关闭。各状态之间的转换流程如图所示。


![](https://img2024.cnblogs.com/other/2625446/202412/2625446-20241215160755802-1917060432.jpg)


**2、退货退款状态机**


退货退款状态机描述了用户申请退货退款时，退款申请单的处理流程和状态转换。核心状态包括待审核、待退货、待收货、售后完成、待买家处理和售后关闭。各状态之间的转换流程如图所示。


![](https://img2024.cnblogs.com/other/2625446/202412/2625446-20241215160756202-1828678665.jpg)



> 本文已收录于，我的技术网站：[tangshiye.cn](https://github.com) 里面有，算法Leetcode详解，面试八股文、BAT面试真题、简历模版、架构设计，等经验分享。


 本博客参考[veee加速器官网](https://youhaochi.com)。转载请注明出处！
