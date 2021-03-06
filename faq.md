# 使用什么 sdk
`zsc` 高度兼容 `ethereum`，可以使用 `ethereum` 的 `sdk`，例如 `web3js`， `web3j `等。

# 使用什么编译器

可以使用网页端[remix](https://remix.ethereum.org)、或者命令行的 [solidity](https://solidity.readthedocs.io/) 编译器进行编译。

# 是否支持EVM？

完全支持以太坊`EVM`，对以太坊开发者完全友好。

# 地址生成规则是否一致？

完全一致。

# 资产如何进入Zenith smart chain？

目前已支持`ZTB`资产，`ZTB`在`ZT`交易平台对`Zenith smart chain`的充提于3月7日上线；`ETH`、`BTC`、`ZUSD`、`LTC`等资产于3月5日上链。

# 有类似swap的Dex合约提供换币吗？

目前官方`Dex`还没有，鼓励社区开发者提供。

# 是否有跨链桥接（bridge）资产到Zenith smart chain？

目前还没有官方的去中心化跨链网桥，鼓励社区开发者提供。
对于开发者资产，我们提供了资产承兑方案，帮组开发者快速资产上链。

参考: [跨链](/bridge.md)

# 如何获取测试币？

官方目前还没有测试币水龙头地址获得`ZTB`。

# 合约部署有什么要注意的吗？

`RPC`接口兼容以太坊，可直接使用`web3.js`，对以太坊开发者完全友好。

# 区块确认时间是怎么样的？

3秒一个区块，20个区块确认

# 简单介绍下Zpos共识机制？

类似于`clique`的`pos+poa`共识机制，支持的最大的`Validator`数量 21个，具有交易成本低、交易延时低、交易并发高等特点。

# 是否支持--pruning 参数

`--pruning`是 `parity` 的参数，`zsc` 的 `API` 遵循 `go-ethereum` 的风格，可以使用 `--gcmode archive` 来实现相同的功能。

# Metamask 卡顿

多发 `mac chrome` 浏览器下，

具体表现是，输入转币数量卡顿、获取 `gasprice` 延迟导致输入为 0，这个问题是一个已知问题，可以参考 `Zsc` 团队给 `metamask` 的提的 issue：
https://github.com/MetaMask/metamask-extension/issues/10202

解决办法如下：

1）使用插件的 `expand view`（扩展视图）模式

![](./images/metamask_lag.png)

2）如果使用多个显示器，将窗口放到主显示器

3）使用其他浏览器