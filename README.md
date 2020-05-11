# NanoPi R2S 专用软件源

![packages](https://github.com/songchenwen/nanopi-r2s-opkg-feeds/workflows/packages/badge.svg)

[看看都包含哪些包](https://github.com/songchenwen/nanopi-r2s-opkg-feeds/tree/master/packages)

----------------

## 添加软件源

在 `软件包 - 配置 - 自定义软件源` 中添加如下一行 

~~~
src/gz songchenwen https://nanopi-r2s-opkg-feeds.songchenwen.com/packages/
~~~

## 添加签名公钥

ssh 进路由器 执行

~~~
mkdir -p /etc/opkg/keys; wget -qO /etc/opkg/keys/5e99c2573f29d764 "https://nanopi-r2s-opkg-feeds.songchenwen.com/keys/5e99c2573f29d764"
~~~

或禁用签名检查，在 `软件包 - 配置` 中删掉这一行 `option check_signature 1`

## 已集成固件

- [songchenwen/nanopi-r2s](https://github.com/songchenwen/nanopi-r2s)

----------------

[欢迎 PR 和 issue](https://github.com/songchenwen/nanopi-r2s-opkg-feeds)

改动 [packages.seed](https://github.com/songchenwen/nanopi-r2s-opkg-feeds/blob/src/packages.seed)。参考其它行的格式，为你想要加的包添加一行，并提交 PR。只要编译能通过我都会合并。

如果你要的包当前 Feeds 里没有，可以对 [add_packages_to_lean.sh](https://github.com/songchenwen/nanopi-r2s-opkg-feeds/blob/src/add_packages_to_lean.sh) 进行改动来添加。
