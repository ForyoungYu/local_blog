---
title: 【Vim】Vim的基本使用
date: 2021-01-08
index_img: /img/vim_use/vim.jpg
banner_img: /img/vim_use/vim_banner.png
tags:
  - Vim
  - Linux
categories:
  - Vim
---

## Linux Vi/Vim

所有的 Unix Like 系统都会内建 Vi 文书编辑器，其他的文书编辑器则不一定会存在。  
在 GNU 项目中，程序员在将 Vi 编辑器移植到开源世界的同时，决定对其作一些改进。  
由于改进后的 Vi 不再是以前 Unix 中的那个原始的 Vi 编辑器了，开发人员也就将它重命名为“Vi improved”，也就是 Vim。  
但是目前我们使用比较多的是 Vim 编辑器。Vim 具有程序编辑的能力，可以主动的以字体颜色辨别语法的正确性，方便程序设计。

## 什么是 Vim

Vim 是从 Vi 发展出来的一个文本编辑器。代码补全、编译及错误跳转等方便编程的功能特别丰富，在程序员中被广泛使用，和 Emacs 并列成为类 Unix 系统用户最喜欢的文本编辑器。

简单的来说， Vi 是老式的字处理器，功能已经很齐全了，但是还是有可以进步的地方。 Vim 则可以说是程序开发者的一项很好用的工具。

**Vim 键位图:**
![Vim 键位图](/img/vim_use/vi-vim.gif)

看起来是不是很复杂？不用担心，但其实常用的也就那么几个，而且命令之间也很具有逻辑性，非常好记。

## Vim 的使用

基本上 Vim 共分为三种模式，分别是**命令模式（Command mode）**，**输入模式（Insert mode）**和**底线命令模式（Last line mode）**。这三种模式的作用分别是：

**命令模式**  
命令模式就是刚刚进入 Vim 的时候默认的模式。

此时如果敲击键盘会被识别为命令。以下是常用的几个命令：

- **i** 切换到输入模式，以输入字符。
- **x** 删除当前光标所在处的字符。
- **:** 切换到底线命令模式，以在最底一行输入命令。

**输入模式**  
在命令模式下按下 i 就进入了输入模式。  
在输入模式中，可以使用以下按键：

- 字符按键以及 Shift 组合，输入字符
- ENTER，回车键，换行
- BACKSPACE，退格键，删除光标前一个字符
- DEL，删除键，删除光标后一个字符
- 方向键，在文本中移动光标
- HOME/END，移动光标到行首/行尾
- Page Up/Page Down，上/下翻页
- Insert，切换光标为输入/替换模式，光标将变成竖线/下划线
- ESC，退出输入模式，切换到命令模式

**底线命令模式**  
在命令模式下按下:（英文冒号）就进入了底线命令模式。  
底线命令模式可以输入单个或多个字符的命令，可用的命令非常多。  
在底线命令模式中，基本的命令有（已经省略了冒号）：

- **q** 退出程序
- **w** 保存文件

按 ESC 键可随时退出底线命令模式。  
简单的说，我们可以将这三个模式想成底下的图标来表示：  
![Vim 的三种工作模式](/img/vim_use/vim_work_mode.png)

## Vim 的按键说明

以上只是基本操作，还有许多的命令可以学习，并且很具有逻辑性。

### 第一部分 一般模式可用的光标移动、选择复制粘贴、搜索替换等

#### 移动光标的方法

|               按键                |                        作用                         |
| :-------------------------------: | :-------------------------------------------------: |
| h 或 向左箭头键(←) 或 [backspace] |                光标向左移动一个字符                 |
|   j 或 向下箭头键(↓) 或 [enter]   |                光标向下移动一个字符                 |
|        k 或 向上箭头键(↑)         |                光标向上移动一个字符                 |
|   l 或 向右箭头键(→) 或 [space]   |                光标向右移动一个字符                 |
|           [Ctrl] + [f]            | 屏幕『向下』移动一页，相当于 [Page Down]按键 (常用) |
|           [Ctrl] + [b]            | 屏幕『向上』移动一页，相当于 [Page Up] 按键 (常用)  |
|           [Ctrl] + [d]            |                屏幕『向下』移动半页                 |
|           [Ctrl] + [u]            |                屏幕『向上』移动半页                 |
|         0 或功能键[Home]          | 这是数字『 0 』：移动到这一行的最前面字符处 (常用)  |
|          $ 或功能键[End]          |          移动到这一行的最后面字符处(常用)           |
|                 H                 |    光标移动到这个屏幕的最上方那一行的第一个字符     |
|                 M                 |     光标移动到这个屏幕的中央那一行的第一个字符      |
|                 L                 |    光标移动到这个屏幕的最下方那一行的第一个字符     |
|                 G                 |           移动到这个档案的最后一行(常用)            |
|                nG                 |         n 为数字。移动到这个档案的第 n 行。         |
|                gg                 |    移动到这个档案的第一行，相当于 1G 啊！ (常用)    |
|             n[Enter]              |          n 为数字。光标向下移动 n 行(常用)          |

> 如果想要进行多次移动的话，例如向下移动 30 行，可以使用 "30j" 或 "30↓" 的组合按键， 亦即加上想要进行的次数(数字)后，按下动作即可！  
> 其实很多的命令只要先加数字都可以实现类似的功能。比如删除命令`dd`，要想删除下两行，可以使用`2dd`。

#### 搜索替换

| 按键  | 作用                                                                                                     |
| :---: | -------------------------------------------------------------------------------------------------------- |
| /word | 向光标之下寻找一个名称为 word 的字符串。例如要在档案内搜寻 vbird 这个字符串，就输入 /vbird 即可！ (常用) |
| ?word | 向光标之上寻找一个字符串名称为 word 的字符串。                                                           |
|   n   | 重复前一个**搜寻**的动作。                                                                               |
|   N   | 与 n 刚好相反，为『反向』进行前一个**搜寻**动作。 例如 /vbird 后，按下 N 则表示『向上』搜寻 vbird 。     |

> 使用 /word 配合 n 及 N 是非常有帮助的！可以让你重复的找到一些你搜寻的关键词！

#### 选择、删除、复制与粘贴

|    按键    | 作用                                                                                                     |
| :--------: | -------------------------------------------------------------------------------------------------------- |
|     v      | 进入按字符选择模式,通过 h、i、j、k 键移动光标选择要进行复制的字符串                                      |
|     V      | 进入按行选择模式，通过 h、i、j、k 键移动光标选择要进行复制的行号                                         |
|  [Ctrl]+v  | 进入到按块选择模式，通过 h、i、j、k 移动鼠标选择要进行复制的区域块                                       |
|     x      | 向后删除一个字符 (相当于 [del] 按键)。                                                                   |
|     X      | 向前删除一个字符(相当于 [backspace] 亦即是退格键) (常用)                                                 |
|     nx     | n 为数字，连续向后删除 n 个字符。举例来说，我要连续删除 10 个字符， 『10x』。                            |
|     dd     | 删除游标所在的那一整行(常用)                                                                             |
|    ndd     | n 为数字。删除光标所在的向下 n 行，例如 20dd 则是删除 20 行 (常用)                                       |
| d1G 或 dgg | 删除光标所在到第一行的所有数据                                                                           |
|     dG     | 删除光标所在到最后一行的所有数据                                                                         |
|     d$     | 删除游标所在处，到该行的最后一个字符                                                                     |
|     d0     | 那个是数字的 0 ，删除游标所在处，到该行的最前面一个字符                                                  |
|     yy     | 复制游标所在的那一行(常用)                                                                               |
|    nyy     | n 为数字。复制光标所在的向下 n 行，例如 20yy 则是复制 20 行(常用)                                        |
| y1G 或 ygg | 复制游标所在行到第一行的所有数据                                                                         |
|     yG     | 复制游标所在行到最后一行的所有数据                                                                       |
|     y0     | 复制光标所在的那个字符到该行行首的所有数据                                                               |
|     y$     | 复制光标所在的那个字符到该行行尾的所有数据                                                               |
|     p      | 将已复制的数据在光标下一行贴上                                                                           |
|     P      | 将已复制的数据在光标上一行贴上                                                                           |
|     J      | 将光标所在行与下一行的数据结合成同一行                                                                   |
|     c      | 重复删除多个数据，例如向下删除 10 行，[ 10cj ]                                                           |
|     u      | **撤销**上一步的操作。(常用)                                                                             |
|  [Ctrl]+r  | **重做（前进）**上一个动作。(常用)                                                                       |
|     .      | 这是就是小数点。表示重复前一个动作。如果你想要重复删除、重复贴上等等动作，按下小数点『.』就好了！ (常用) |

> u 与 [Ctrl]+r 是很常用的指令，表示前进和后退。另外「.」这个指令表示重复刚刚的动作，也非常常用。

### 第二部分：一般模式切换到编辑模式的可用的按钮说明

| 按键  | 作用                                                                                                                                            |
| :---: | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| i, I  | 进入输入模式(Insert mode)：i 为『从目前光标所在处输入』， I 为『在目前所在行的第一个非空格符处开始输入』。 (常用)                               |
| a, A  | 进入输入模式(Insert mode)：a 为『从目前光标所在的下一个字符处开始输入』， A 为『从光标所在行的最后一个字符处开始输入』。(常用)                  |
| o, O  | 进入输入模式(Insert mode)：这是英文字母 o 的大小写。o 为在目前光标所在的下一行处输入新的一行； O 为在目前光标所在的上一行处输入新的一行！(常用) |
| r, R  | 进入取代模式(Replace mode)：r 只会取代光标所在的那一个字符一次；R 会一直取代光标所在的文字，直到按下 ESC 为止；(常用)                           |
| [Esc] | 退出编辑模式，回到一般模式中(常用)                                                                                                              |

### 第三部分：一般模式切换到指令行模式的可用的按钮说明

#### 指令行的储存、离开等指令

|        按键         | 作用                                                                                                                      |
| :-----------------: | ------------------------------------------------------------------------------------------------------------------------- |
|         :w          | 将编辑的数据写入硬盘档案中(常用)                                                                                          |
|         :w!         | 若文件属性为『只读』时，强制写入该档案。不过，到底能不能写入， 还是跟你对该档案的档案权限有关啊！                         |
|         :q          | 离开 vim (常用)                                                                                                           |
|         :q!         | 若曾修改过档案，又不想储存，使用 ! 为强制离开不储存档案。                                                                 |
|         :wq         | 储存后离开，若为 :wq! 则为强制储存后离开 (常用)                                                                           |
|         ZZ          | 这是大写的 Z 喔！如果修改过，保存当前文件，然后退出！效果等同于(保存并退出)                                               |
|         ZQ          | 不保存，强制退出。效果等同于 :q!。                                                                                        |
|    :w [filename]    | 将编辑的数据储存成另一个档案（类似另存新档）                                                                              |
|    :r [filename]    | 在编辑的数据中，读入另一个档案的数据。亦即将 『filename』 这个档案内容加到游标所在行后面                                  |
| :n1,n2 w [filename] | 将 n1 到 n2 的内容储存成 filename 这个档案。                                                                              |
|     :! command      | 暂时离开 vi 到指令行模式下执行 command 的显示结果！例如『:! ls /home』即可在 vi 当中察看 /home 底下以 ls 输出的档案信息！ |

> 注意一下啊，那个惊叹号 (!) 在 vi 当中，常常具有『强制』的意思～

## 其他技巧

### 批量注释

[Ctrl] + v 进入块选择模式，然后移动光标选中你要注释的行，再按大写的 I 进入行首插入模式输入注释符号如 // 或 #，输入完毕之后，按两下 ESC，Vim 会自动将你选中的所有行首都加上注释，保存退出完成注释。

取消注释：

[Ctrl] + v 进入块选择模式，选中你要删除的行首的注释符号，注意 // 要选中两个，选好之后按 d 即可删除注释，ESC 保存退出。

> 本文参考：[菜鸟编程 Linux vi/vim](https://www.runoob.com/linux/linux-vim.html)