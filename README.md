# `laincloud/centos-lain` box 的打包程序

## 与 [flex 版本](https://github.com/frostynova/bento) 的不同

合并了 [chef/bento](https://github.com/chef/bento) [Fix new-style device
naming from Network Manager on RHEL/CentOS
7](https://github.com/chef/bento/commit/d0c2e56fcc4ec81e152af6c5fbdf1f115f976e95) 的修改

## 与 [chef/bento](https://github.com/chef/bento) 的不同

合并了 flex 对 [Predictable Network Interface
Names](https://www.freedesktop.org/wiki/Software/systemd/PredictableNetworkInterfaceNames/) 禁用

## [最终的脚本](https://github.com/kaizhang-shanxi/bento/blob/master/scripts/centos/cleanup-lain.sh)

## 打包过程

```
git clone https://github.com/kaizhang-shanxi/bento  # 下载打包程序

# 需要一个 centos 的 dvd
brew install packer   # 当时 flex 的步骤，但我忘了是不是必需的了。。。

cd bento
bin/bento build  -m file:///Users/flex/Soft/ISO/ centos-lain-7.2-x86_64.json
```

> **重要**：是 `cent-lain-7.2-x86_64.json`，不是 `cent-7.2-x86_64.json`。
