# 升级：部署一个 ERC20 代币

现在，您已经成功部署并与第一个智能合约进行了交互，是时候更进一步了！在接下来的部分，我们将指导您通过 OpenZeppelin 提供的经过验证的 ERC20🪙 实现，来部署您自己的 ERC20 代币。让我们开始在 Open Campus Codex 网络上创建属于您的代币吧！

### 什么是 OpenZeppelin？

OpenZeppelin 是一个安全智能合约开发库，提供了流行代币标准的实现，包括 ERC20，您可以使用这些实现来创建自己的代币，而无需重新发明轮子。使用 OpenZeppelin 的实现可以确保您的代币遵循 Ethereum 生态系统中的最佳实践和标准。

从了解合约的基本结构开始，让我们创建一个 `SampleERCToken` 合约。

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract SampleERCToken {
}
```

### 导入 OpenZeppelin ERC20

在您的 `TokenPoken.sol` 文件中，首先通过以下语句导入 OpenZeppelin 的 ERC20 实现：

```solidity
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
```

这允许您继承 ERC20 合约并基于它构建您的代币。OpenZeppelin 提供了一个安全、经过验证的 ERC20 代币基础。

### 编写代币合约

接下来，通过编写合约代码来定义您的 ERC20 代币。使用名称 "TokenPoken" 和符号 "TP" 作为 ERC20 构造函数的参数。确保构造函数为空，只调用 `ERC20` 构造函数：

有关 ERC20 合约的更多详细信息，请参阅 [OpenZeppelin 文档](https://docs.openzeppelin.com/contracts/4.x/erc20)，以了解其功能和特性。

以下是一个起点：

```solidity
contract SampleERCToken is ERC20 { 
	// ...
}
```

这段代码定义了您的代币的基本结构，使用 OpenZeppelin 的合约来确保安全和简便。

### 编译合约

要进行编译，打开您的 Solidity IDE 并选择 **0.8.23** 编译器版本。点击“编译”，确保没有错误，并且绿色勾号应确认编译成功。

### 部署合约

如果您使用的是 Solide IDE，在 **Build & Deploy Tab**（构建与部署标签）中，选择 `SampleERCToken` 并点击 **Deploy**（部署）。

### 测试您的代币

一旦 `TokenPoken` 合约部署成功，您就可以与其继承的 ERC20 函数进行交互。以下是一些可以尝试的操作：

- 🧮 **查看总供应量：** 调用 `totalSupply` 来查看 TokenPoken 的总供应量。
- 👛 **查看您的余额：** 使用 `balanceOf` 并输入您的地址查看代币余额。
- 🔄 **转账代币：** 尝试使用 `transfer` 函数将代币发送到另一个钱包。

### ❗提交部署到 Proof of Learn

如果您之前部署了 `SimpleContract`，现在可以对 `SimpleERCToken` 执行相同操作。恭喜！您已成功创建并部署了名为 TokenPoken、符号为 TP 的 ERC20 代币，使用 OpenZeppelin 的 ERC20 合约。这一练习展示了使用 OpenZeppelin 进行安全和标准化智能合约开发的强大与便捷。

确保在 Proof of Learn 平台上领取 **免费 POL POAP**，展示您在 Open Campus Codex 上成功部署和交互智能合约的成就！ 🎉🎉🎉