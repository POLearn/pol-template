# 与智能合约的交互

### 介绍

在部署您的第一个合约的最后部分，让我们学习如何通过使用 setter 方法来交互并更新 `name` 变量 🔧

> 先决条件：确保您已安装 MetaMask 并连接到 Open Campus Codex 网络，且 `SimpleContract` 合约已成功部署。

### 与合约交互

现在，您的 `SimpleContract` 已部署在 Open Campus Codex 网络上，我们将使用 `set` 方法将 `name` 变量更改为 `Vitalik`，并检索交易哈希以验证交易。

#### 调用 set 方法

首先，找到合约界面中的 `set` 函数。在输入框中输入 **Vitalik** 并点击“Transact”。MetaMask 会提示您确认交易——批准交易并等待交易被处理。

#### 验证合约的状态

交易确认后，调用合约中的 `name` 函数以检查当前值。如果返回的是 `Vitalik`，恭喜！您已经成功与合约交互并更新了其状态。🎉

### ❗将交易提交给 Proof of Learn

为了验证此任务，提交交易哈希到 Proof of Learn (POL) 平台。这将确认您已经成功与智能合约进行了交互。