---
layout: post
title:  "ubuntu上安装swift"
date:   2020-09-15 09:30:51 +0800
categories: [iOS]
tags: [swift]
---


1. 安装依赖关系：

```
sudo apt-get install clang libicu-dev
```

2. 下载 swift：

```
wget https://swift.org/builds/swift-4.1-release/ubuntu1404/swift-4.1-RELEASE/swift-4.1-RELEASE-ubuntu14.04.tar.gz
```

3. 解压：

```
tar xzf swift-4.1-RELEASE-ubuntu14.04.tar.gz
```

4. 配置环境变量：

```
vim ~/.bashrc
export PATH=~/swift-4.1-RELEASE-ubuntu14.04/usr/bin:"${PATH}"
source ~/.bashrc
```


5. 验证是否安装成功：

```
swift --version

```

输出：

```
Swift version 4.1 (swift-4.1-RELEASE)
Target: x86_64-unknown-linux-gnu
```