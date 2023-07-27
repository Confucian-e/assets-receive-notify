# MetaMask Snaps 收到资产提醒

现在的 MetaMask 在用户收到 ETH 和 ERC20 代币等资产时没有提醒。然而现实生活中，当你的账户收到转账时会自动提醒，所以可以利用 Snaps 来实现这一功能。

## 实现原理

访问节点，监听交易

- ERC20 等合约代币类可通过监听 Transfer 事件来触发提醒
- ETH 可通过计算新区块的账户余额变化或监听 tx 的 value 字段来触发提醒

## 配置

需要启用 Snaps 的 `endowment:ethereum-provider` 权限和 `snap_notify` API

参考文档：

- https://docs.metamask.io/snaps/reference/permissions/#endowmentethereum-provider
- https://docs.metamask.io/snaps/reference/rpc-api/#snap_notify