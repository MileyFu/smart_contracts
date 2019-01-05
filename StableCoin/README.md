# CyberMiles Stable Coin Smart Contract

This stable coin smart contract (CMTD) is designed to work in conjunction with a payment gateway. At present the contract inherits 4 pre-existing contracts from [OpenZeppelin](https://github.com/OpenZeppelin/openzeppelin-solidity).

It was found that the following 4 OpenZeppelin contracts inherit from and implement a variety of contracts and libraries which in-turn provide sufficient functionality to implement the CyberMiles Stable Coin Smart Contract (CMTD).

Below is a quick overview of what all of the 4 inherited contract bring to the CMTD contract. The most significant functionality is the ability to mint and burn tokens as well as the ability to manage roles as apposed to the traditional method of just having the owner perform all of the administration functions (i.e. using the Ownable contract). 

Any additional functionality can now be added to the CMTD contract in the form of function overrides and/or additional modifiers.

## Mintable
The OpenZeppelin ERC20Mintable contract inherits from ERC20 and MinterRole. MinterRole subsequently implements the Roles Library. The Roles Library manages addresses which are assigned to a single role. Using the ERC20Mintable contract provides not only the ability to mint new tokens, but the ability to completely manage access control for one or more "minters" which are technically an instance of Roles.Role.

## Burnable
The OpenZeppelin ERC20Burnable contract inherits from ERC20. It has a function called burnFrom which allows a specific amount of tokens from the target address to be burned. The burning of tokens is on the proviso that an allowance to do so has been set.

## Pausable
The OpenZeppelin ERC20Pausable contract inherits from ERC20 and Pausable. Pausable inherits from PauserRole. PauserRole subsequently implements the Roles Library. The Roles Library manages addresses which are assigned to a single role, as we mentioned in the Mintable section.

## Detailed
The OpenZeppelin ERC20Detailed contract is IERC20 and simply provides an opportunity to enrich the contract with additional name, symbol and number of decimals for the token.

All in all, the above 4 contracts (and their inherited contracts and implemented libraries) provide the following functionality to the CMTD contract without any modification whatsoever. As mentioned any additional functionality can be created through the use of function overriding and/or additional modifiers.

## Functionality

![Functionality](images/functionality.png)

## Supply
The CMTD contract is designed to have a variable supply. The initial supply is set to zero. Tokens minted will increase the supply and tokens burned will decrease the supply. The minting and burning of tokens will come about as a result of logic in the payment gateway.

# CyberMiles稳定币智能合约

该稳定币智能合约 (CMTD)为和支付网关共同使用的设计。目前该合约继承了4个已经存在的 [OpenZeppelin](https://github.com/OpenZeppelin/openzeppelin-solidity)的合约。

发现一下 4 OpenZeppelin 合约继承并执行了一系列多种合约和库，反过来提供了充足的功能从而可以实现CyberMiles稳定币智能合约 (CMTD).

 下面简要概述了4个继承的合约对CMTD合约的影响。最重要的功能是铸造和销毁token的能力以及管理角色的能力，相对于传统的方法（即使用Ownable合约），只可以让所有者执行所有管理功能。

现在可以以函数覆盖和/或其他修饰符的形式将任何额外的功能都能呗加入到 CMTD 合约。

## 可铸造
OpenZeppelin ERC20可铸造合约继承自ERC20和MinterRole。 MinterRole随后实现了角色库。角色库管理分配给单个角色的地址。使用ERC20Mintable合同不仅提供了铸造新token的能力，还提供了完全管理一个或多个“铸造者minters”的访问控制的能力，这些“铸造者minters”在技术上是Roles.Role的一个实例。

## 可销毁
The OpenZeppelin ERC20可销毁合约继承自ERC20。它有一个名为burnFrom的函数，允许铸造目标地址中的特定数量的token。token销毁的前提是已经设定了这样做的额度。

## 可暂停
OpenZeppelin ERC20可暂停合约继承自ERC20和Pausable。 Pausable继承自PauserRole。 PauserRole随后实现了角色库。角色库管理分配给单个角色的地址，正如我们在Mintable部分中提到的那样。


## Detailed细节说明
The OpenZeppelin ERC20细节合约是IERC20，只是提供了一个丰富合约的机会，能够加附加名字，标志和token的小数位数。

总而言之，上述4个合约（及其继承的合同和实施的库）为CMTD合同提供了以下功能，没有任何修改。 如上所述，可以通过使用函数覆盖和/或附加修饰符来创建任何附加功能。

## 功能

![Functionality](images/functionality.png)

## 供应
CMTD 合约设计成了可变供应量。初始供应量设为0。铸造的token将增加供应量，燃烧的代币将减少供应量。 token的铸造和销毁将是支付网关逻辑的结果。


