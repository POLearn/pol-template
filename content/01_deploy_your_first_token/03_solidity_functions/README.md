# 函数  

### 介绍  

现在我们已经设置了一个包含状态变量的合约，接下来让我们深入了解如何通过函数与这些变量进行交互。  

### 函数定义  

在我们的 `SimpleContract` 中使用函数之前，我们需要先定义它。在 Solidity 中，函数使用 `function` 关键字定义，后面跟着一个唯一的函数名、可选的参数列表以及用大括号 `{}` 包裹的语句块。基本 **语法** 如下：  

```solidity  
function functionName(int arg1, string memory arg2, ...) visibility stateMutability returns() {
   // 逻辑写在这里 :)  
}
```  

### 函数名  

函数名必须是唯一的，通过这个名字 (`functionName`) 您可以调用该函数。  

### 参数  

参数部分定义了函数的参数，例如 `arg1` 是一个整数，而 `arg2` 是存储在内存中的字符串；根据需要可以添加其他参数。  

### 可见性 (Visibility)  

这决定了函数的访问级别，例如 `public`、`private` 或 `internal`，用于定义谁可以调用该函数。  

### 状态可变性 (State Mutability)  

> ⚠️ **注意**：我们将在下一个资源中介绍作用域的概念！  

状态可变性指示函数是否可以修改合约的状态，例如 `pure`、`view` 或 `nonpayable`，并影响其与区块链的交互方式。  

### 返回类型  

返回类型指定了函数调用时的输出值类型；如果函数有返回值，可以在括号中注明类型。  

例如，`returns(uint)` 表示函数将返回一个无符号整数：  

```solidity  
function getValue() public view returns(uint) {
	return 1;  
}
```  

### 任务 📝  

向您的 `SimpleContract` 添加以下函数，让用户可以设置 `name` 状态变量：  

```solidity  
function set(string memory _name) public;  
```  

这个函数接受一个字符串参数 `_name` 并更新合约中的 `name` 变量。  