# 与智能合约交互

在本节中，我们将学习如何通过使用设置方法更新 `name` 变量来与已部署的智能合约进行交互 🔧

> 前提条件：确保您已经安装了 MetaMask，并连接到 EDU Chain Testnet 网络，且您的 `SimpleContract` 已成功部署。

### 与合约交互

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract.png)

现在，您的 `SimpleContract` 已部署在 EDU Chain Testnet 网络上，让我们使用 `set` 方法将 `name` 变量的值更新为 `Vitalik`，并检索交易哈希以验证交易。

### ❗任务：调用 `set` 方法

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract_set.png)

您可以点击合约界面中的 `set` 方法。由于合约只有一个参数，您将能够输入 `name` 的值。输入 **Vitalik** 并点击 *Send*。这将提示您确认交易并批准它。

### 与合约状态交互

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract_name.png)

一旦交易确认，通过调用合约中的 `name` 方法来检查其当前值。如果返回 `Vitalik`，恭喜您！您已经成功与合约交互并更新了合约的状态 🎉

您可以将 `set` 方法的交易提交到 Proof of Learn (POL) 平台，完成此任务。这将确认您已成功与 EDU Chain 上的智能合约进行交互。