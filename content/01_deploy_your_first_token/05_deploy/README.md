# 部署智能合约  

### 介绍  

在我们学习了 Solidity 的基础知识，包括合约结构、状态变量、函数定义和状态可变性之后，接下来就是部署 `SimpleContract` 合约的时刻了！🚀  

### 添加 Open Campus Codex 网络  

要将您的合约部署到 Open Campus Codex 网络，您需要将这个自定义网络添加到 MetaMask 中。请按照以下步骤操作，并使用表格中提供的详细信息：  

1. 打开 MetaMask，点击顶部的网络下拉菜单。  
2. 选择“添加网络”，并填写以下信息：  

| **字段**              | **详细信息**                              |
|-----------------------|------------------------------------------|
| **网络名称**          | Open Campus Codex                        |
| **新 RPC URL**        | `https://open-campus-codex-sepolia.drpc.org` |
| **链 ID**             | `656476`                                 |
| **货币符号**          | `EDU`                                    |
| **区块浏览器 URL**    | `https://opencampus-codex.blockscout.com/` |

添加这些详细信息后，您将连接到 Open Campus Codex 网络，并准备好部署您的合约！🎉  

### 编译合约  

- 将 Solidity 编译器版本设置为 **0.8.23**。  
- 编译之前示例中的 `SimpleContract` 合约。  

### 部署合约  

- 编译后，将 `SimpleContract` 部署到 Open Campus Codex 网络。MetaMask 会提示您批准部署交易。  

交易确认后，您的合约成功部署！  

恭喜！您已经成功配置了 MetaMask 以连接 Open Campus Codex 网络，并成功部署了 Solidity 合约，现在可以与其进行交互了。🎉  

### ❗将部署结果提交给 Proof of Learn  

要完成此任务并提交给 Proof of Learn (POL)，请将您部署的合约交易提交到 POL 平台。这将确认您已经成功部署了合约，并可以获得一个 🏆**POL POAP**。  

### 结论  

现在您的合约已部署，接下来就可以深入学习！在下一部分中，我们将探讨如何与部署的合约交互，更新 `name` 变量，并使用函数修改合约的状态。敬请期待⚡