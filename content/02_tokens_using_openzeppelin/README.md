### 部署 ERC20 代币

在掌握了智能合约的基础知识，并使用 EDU Chain 与它们进行交互后，现在是时候更进一步了！在本节中，我们将引导您通过 OpenZeppelin 久经考验的 ERC20 🪙 实现来部署您自己的 **ERC20 代币**。

### 什么是 OpenZeppelin？

在我们深入研究合约之前，先来了解一下 OpenZeppelin。OpenZeppelin 是一个用于安全智能合约开发的库。它提供了流行的代币标准（包括 ERC20）的实现，您可以利用这些实现来创建自己的代币，而无需从头开始开发。使用 OpenZeppelin 的实现可以确保您的代币符合以太坊生态系统中的最佳实践和标准。

从了解合约的基本结构开始，我们将创建一个 `SampleERCToken` 合约。请在您喜欢的 IDE 中加载模板合约：[SampleERCToken.sol](https://github.com/POLearn/pol-template/blob/master/contracts/SampleERCToken.sol)。

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/token_load.png)

我们可以看到这是一个空合约，但值得注意的是其中包含了 OpenZeppelin 的 `ERC20` 合约的导入。让我们仔细看一下这段代码：

```solidity
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
```

这允许您继承 ERC20 合约，并在其基础上构建自己的代币。OpenZeppelin 提供了一个安全、久经考验的 ERC20 代币基础。

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/token_setup.png)

查看构造函数时，它接收 `name` 和 `symbol` 参数。而剩下的代码则是用于代币的铸造和转账的实现，所有这些都已经为您完成了。

现在让我们在主合约中继承它。回到 `SampleERCToken`，确保您的合约继承自 `ERC20`，如下所示：

```solidity
contract SampleERCToken is ERC20
```

在构造函数中，我们也需要调用 ERC20 的构造函数：

```solidity
constructor() ERC20("TokenName", "TOKEN") {
}
```

我们将通过编写合约代码来定义 ERC20 代币。使用 "TokenPoken" 作为名称，"TP" 作为符号传递给 ERC20 构造函数。请确保构造函数中仅调用 `ERC20` 构造函数：

更多关于 ERC20 合约的详细信息，请参考 [OpenZeppelin 文档](https://docs.openzeppelin.com/contracts/4.x/erc20) 来了解其功能和特性。

### 编译合约

与之前的合约一样，请确保您使用的是正确的 Solidity 编译器版本。在本次练习中，我们将使用 **0.8.23**。使用正确的版本非常重要，因为不同版本的功能和语法可能有所不同。

### 部署合约

一旦合约编译完成，将 `SampleERCToken` 部署到我们连接的 EDU Chain 测试网。MetaMask 将提示您批准部署交易。

### 测试您的代币

当您的 `TokenPoken` 合约部署完成后，您可以与其继承的 ERC20 功能进行交互。以下是一些可尝试的操作：

- 🧮 **查看总供应量：** 调用 `totalSupply` 查看 TokenPoken 的总供应量。
- 👛 **查看您的余额：** 使用您的地址调用 `balanceOf` 查看您的代币余额。
- 🔄 **转账代币：** 使用 `transfer` 函数将代币发送到另一个钱包。

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/token_name.png)

### ❗任务：代币部署

如果您之前部署过 `SimpleContract`，现在可以用相同的方法部署 `SampleERCToken`。恭喜您！您已经成功使用 OpenZeppelin 的 ERC20 合约创建并部署了自己的 ERC20 代币 TokenPoken，其符号为 TP。这次练习展示了使用 OpenZeppelin 进行安全和标准化智能合约开发的强大功能和便利性。

别忘了领取来自 Proof of Learn 的 **POL POAP** 奖励，以证明您已在 EDU Chain 上成功部署并交互智能合约！🎉🎉🎉