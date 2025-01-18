### 部署智能合约

在学习了 Solidity 的基础知识后，包括合约结构、状态变量、函数定义和状态可变性，现在是时候部署 `SimpleContract` 合约了！🚀

### 在 MetaMask 中添加 EDU Chain 网络

要将合约部署到 EDU Chain 测试网，您需要将自定义网络添加到 MetaMask。

1. 打开 MetaMask，点击顶部的网络下拉菜单。  
2. 选择“添加网络”，并填写以下信息：  

| **字段**               | **详细信息**                                 |
|-----------------------|---------------------------------------------|
| **网络名称**            | EDU Chain 测试网                            |
| **新 RPC URL**         | `https://open-campus-codex-sepolia.drpc.org` |
| **链 ID**              | `656476`                                    |
| **货币符号**            | `EDU`                                       |
| **区块浏览器 URL**      | `https://edu-chain-testnet.blockscout.com/`  |

完成这些步骤后，您将连接到 EDU Chain 测试网并准备部署您的合约！🎉

### 设置合约

接下来加载一个合约模板。在您喜欢的 IDE 中加载此合约。理想情况下，您可以使用 PoL 的互动式 IDE。使用以下 URL 提供模板：  
`https://github.com/POLearn/pol-template/blob/master/contracts/SimpleContract.sol`。

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract_load.png)

```solidity
string public name;

function set(string memory _name) public {
    name = _name;
}
```

#### 合约解析

`set` 函数是一个 setter 函数，允许用户动态更新 `name` 状态变量。它接收一个参数 `_name`（类型为 `string`），该参数在函数调用时提供，并将其赋值给合约中存储的 `name` 变量。这使合约更加互动，用户可以实时更新信息，例如重命名代币或根据输入定制合约数据。

### 编译合约

确保您使用正确的 Solidity 编译器版本。本次练习中，我们使用 **0.8.23** 版本。使用正确的版本至关重要，因为不同版本之间功能和语法可能有所差异。

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract_version.png)

### 部署合约

编译完成后，将 `SimpleContract` 部署到我们已连接的 EDU Chain 测试网。MetaMask 会提示您批准部署交易。

交易确认后，您的合约将成功部署！🎉 您还可以通过以下配置连接到 **EDU Chain 主网**：

| **字段**               | **详细信息**                              |
|-----------------------|------------------------------------------|
| **网络名称**            | EDU Chain                              |
| **新 RPC URL**         | `https://rpc.edu-chain.raas.gelato.cloud` |
| **链 ID**              | `41923`                                 |
| **货币符号**            | `EDU`                                   |
| **区块浏览器 URL**      | `https://edu-chain.blockscout.com/`      |

### ❗任务：将合约提交到 PoL

要完成 POL 平台上的此任务，请将您部署的合约交易提交到 Proof of Learn (POL) 平台。这将确认您已成功部署合约。完成后，您将获得 🏆**POL POAP** 作为奖励。

现在合约已部署，下一步我们将深入了解如何与已部署的合约互动、更新 `name` 变量以及通过其函数修改合约状态⚡！