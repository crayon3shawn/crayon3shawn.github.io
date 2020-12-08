---
title: 從Homebrew學習terminal介面
date: 2020-12-03 01:24:34
tags:
    - Homebrew
    - Terminal
    - Mac
categories: 技術筆記
---
## 什麼是Homebrew

Homebrew是套件管理軟體
第一次碰homebrew，是在大一的時候
雖然是資工系的，但對terminal指令不熟還真的是蠻慚愧的
那時候完全不懂這個東西是什麼用途
最近這陣子才開始研究，跟體驗到他的方便性。
也是從homebrew開始熟悉terminal這個環境，很推薦用這個來學習

可以用command line安裝軟體就是潮(x)

比起以往下載dmg，然後同意，下一步下一步，拖拉到應用程式資料夾，homebrew只需要，例如：

``` zsh
EX: brew install anaconda
```

就可以安裝軟體或是套件了

macOS在反安裝非appstore的軟體時都還要用像是Appcleanr的第三方軟體移除，但homebrew 只需要一條指令就可以移除乾淨。

``` zsh
EX: brew uninstall anaconda
```

像是adobe cloud這類圖形化介面的軟體，也是能夠透過homebrew-cask安裝，部分的字形也是能夠透過
指令在經過改版之後，也都變成brew 指令就能操作了，方便許多

如果設定好的話，將來可以用brewfile在clean install時，來大量安裝

Homebrew的官網也有繁體中文，安裝有問題都可以去官網看說明

不過網路上的有些文章指令已經過期了，看其他部落格時，可能要注意一下指令是不是正確的。

## 怎麼安裝Homebrew

需要先安裝xcode的commandline，不用安裝完整的xcode

``` zsh
# 安裝 command line tools
xcode-select --install
```

``` zsh
# 可以確認xcode command line有沒有安裝，如果有路徑就是OK的
xcode-select -p
```

然後安裝Homebrew，下面是官方推薦的安裝方式

``` zsh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Homebrew的基本操作指令

基本上去看[Homebrew的官方網站](https://brew.sh/index_zh-tw)，指令應該都最詳細啦，或是去看homebrew的github。但還是稍微提一下。

或是可以直接查看指令

``` zsh
brew help
```

安裝單一軟體

``` zsh
brew install [formula]
```

更新 homebrew

``` zsh
brew update
```

更新單一軟體

``` zsh
brew upgrade [formula]
```

更新全部軟體

``` zsh
brew upgrade --all
# or
brew upgrade -a
```

清除brew產生的暫存檔或遺留的殘檔

``` zsh
brew cleanup
```

像2019的文章可能還是會寫

``` zsh
brew cask install chrome
```

但現在只需要

``` zsh
brew install chrome
```

## 我把Homebrew拿來做什麼

### brewfile

### dotfile

建立dotfile && 建立brewfile
<https://blog.spencerwoo.com/2020/07/how-i-manage-my-dotfiles/>
<https://github.com/TheLocehiliosan/yadm>
<https://yadm.io/docs/getting_started>
<https://github.com/dotfiles/dotfiles.github.com>
<https://medium.com/@webprolific/getting-started-with-dotfiles-43c3602fd789>

Getting Started With Dotfiles
<https://medium.com/@webprolific/getting-started-with-dotfiles-43c3602fd789>

<https://github.com/zhangchenchen/clean-dotfile/blob/master/README_ZH_CN.md>

### minconda

## 參考資料

深入淺出xcode command line tool
<https://jamesdouble.github.io/blog/2019/12/19/xcCmdLine-1>
更快速、簡潔、優雅地管理你的 Mac 軟體套件
<https://www.onejar99.com/mac-homebrew-homebrew-cask-mac/>
Homebrew
<https://brew.sh/index_zh-tw.html>
