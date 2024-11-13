# Move 语言基础

Move 语言起初是一个通用型的语言，后来演化成了两个分支 aptos 和 Sui，两者都在 move 语言的基础上增加了一些在自己特定语言上使用的函数和库。

本教程也会基于 [sui 下的 move](https://github.com/move-language/move-sui) 展开。

> P.S. move 语言在 sui下的发展已经不在原仓库里面维护了，而是在 [MystenLabs/sui 的 external-crates/move ](https://github.com/MystenLabs/sui/tree/main/external-crates/move) 文件夹中管理，因此你可以看到 `move-language/move-sui` 中基本没有了什么 commit 提交

## 安装 move 环境
目前来说 move语言已经被内置到了 sui cli 中，因此我们可以通过安装 sui 命令行来体验 move语言。其次如果你只关注与 move 语言本身，可以通过编译[move-sui](https://github.com/MystenLabs/sui/tree/main/external-crates/move) 来获得一个纯净的move语言解析器和VM。

在确保电脑已经配置好了 Rust 的开发环境后，我们可以通过下面的命令来安装 sui 开发网络的命令行工具
```shell
cargo install --locked --git https://github.com/MystenLabs/sui.git --branch devnet sui
```

安装完成后，通过下面的命令来测试是否安装成功：
```shell
sui --version
```
输出结果类似于以下就意味着安装成功了。
```
sui 1.38.0-1c9699994e34
```
