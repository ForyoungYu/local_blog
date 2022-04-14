---
title: "我与Linux的故事"
date: 2022-04-11
tags:
  - Linux
categories:
  - 随笔
---

# 我与 Linux 的故事

目前我使用的操作系统是 Linux，除了玩游戏和一些特殊文档编辑以及阅读论文等需要切换到 Windows，剩下的时间都是在用 Linux。

## 初遇

第一次接触 Linux 是在 2018 年春，那一年我大二。一次偶然的机会我打开了 deepin 操作系统的官方网页，那一刻我被 deepin 的操作界面吸引住了，才知道操作系统原来可以这么漂亮。这是我第一次了解到 Linux。

2018 年末，我终于在自己的电脑成功安装上 deepin，第一次使用的感觉其实说实话并不是那么得好用。由于使用 Windows 的习惯，安软件都安不上，只能在应用商店里面找应用，而且软件也都不是最新版的，可以说那次的体验是极差的，但我也使用了一段时间，学习了一些 Linux 的基本知识，用它来写写爬虫啥的（那时候对爬虫挺感兴趣），当时使用的 IDE 是 sublime text。

## 启蒙

转眼到了 2020 年，这一年是我对 Linux 进行探索的开始。从这一年我对 Linux 的认知发生了很大的变化，可能我对 Linux 有缘分，我突然觉得在 Linux 下编程是一件很容易的事情，对比反而觉得在 Windows 下编程很复杂，因为 Linux 的文件系统在我看来十分的简洁（一切都从“/”开始的文件结构，不像 Windows 的各种盘符和反斜杠），我开始逐渐理解了 Linux 的思想极其设计理念，感觉这才是真正的操作系统。同时这一年经过学习也知道了原来 Linux 是有很多的发行版的，每个发行版也各具特色，选择一款适合自己的 Linux 是一件很重要的事情，于是我展开了对 Linux 的探索之路。这时我使用的 IDE 是 vscode。

我喜欢刷 b 站，一次偶然我刷到了 TheCW 的视频，这才彻底打开了我对 Linux 的兴趣阀门。cw 的视频给我展示了许多我未曾见到过的 Linux 操作，让我见识到了 Linux 的另一面。在他的视频中我认识到了 manjaro 和 Arch 操作系统以及许许多多的开源工具，如 ranger、vim、zsh、git 等，简直颠覆了我对以往 Linux 的认知，原来这才是 Linux 应有的样子。那段时间我经常反复看他的视频学习，也跟着它学习安装操作系统，学着自己解决问题，IDE 也从 vscode 逐渐过渡到了 vim。我也尝试了许多其他的 Linux 发行版如 Ubuntu、manjaro、Mint 甚至地狱级别的 Arch（其实也不算多难），学着配置自己的操作系统，搭建属于自己的环境，将自己的配置文件保存到 github 上，那时我觉得 Linux 是神一样的存在。那段时间 cw 的视频更新也很频繁，每一期我都会看，那时候自己的技术也不是很扎实，装好的 Arch 经常一遇到问题就重装系统，装了又卸（我装 Arch 的最短纪录为 30 分钟，后来才知道遇到的问题其实都是可以解决的），自我估计到目前为止我装系统的次数不下一百次，在装系统的过程中我也学到了很多的知识。

那段时间我一直模仿 cw 大佬的配置，使用 Arch 作为自己的 Linux，后来由于考研的原因就停止学习了一段时间。

## 发芽

这一阶段是我对 Linux 有了自己的见解。

时间来到 2021 年，考研结束的我有开始了折腾 Linux，这是的我对 Linux 逐渐开始有了系统性的认识，一些常规的命令都会操作，也开始逐渐完善自己的配置文件。为了向极客靠拢（为了装逼），我开始学习 vim 以及如何配置插件，当然配置的不很到位。这段时间我使用的还是 Arch，偶尔换到 manjaro 上面，Arch 的自由度非常高，他不同于其他的 Linux 发行版，Arch 可以说是个 DIY 性质的 Linux，他不会预装多余的软件，安装好它之后只是一个不断闪烁的命令提示符，没有其他多余的东西，用户可以再此基础上安装自己想装的桌面环境，那时我主要在 Gnome 和 kde 桌面反复横跳，期间也尝试一些小众的桌面管理器如 i3 和 dwm。因为各有各的优点不知选哪一个好 😂，由此我也展开了长达一年半多的 Linux 美化之路（这是个坑，千万别跳进来）。我承认自己是条颜狗，喜欢漂亮的东西，操作系统也不例外，经常是装了 Gnome 配置不好又贪恋 kde，换到 kde 又思念 Gnome 的简洁高效，来回反复了折腾无数次，说多了都是泪。

Arch 作为最能折腾的操作做系统我也玩了将近一年，后来认识到该邪教（在 Linux 发行版圈子里，其他发行版都称 Arch 为邪教组织）的真实模样，我来给大家总结一下：

1. Arch 的软件包是我见过最多的 Linux 发行版，尤其是 aur，几乎没有搜不到的软件。
2. Arch Linux 确实是一个不错的 Linux 发行版，他属于滚动更新的，即所有的包都会是最新版的版本，这就给它带来不稳定的因素，比如长时间不更新容易滚挂的风险，我可不想使用用着用着就会挂掉的系统，我需要一个稳定的操作系统。
3. Arch 配置起来很麻烦，一切都是从头开始配置自己的系统，做不到开箱即用，甚是折腾，对于忙于学业的我来说这会耗费极大的时间和精力。

后来因为逐渐意识到 Arch 不适合自己，但又想体验 Arch 丰富的软件，于是我退而求其次试用起了 manjaro，manjaro 是基于 arch 开发的 Linux 发行版，能够做到开箱即用，说白了就是将 Arch 向其他 Linux 发行版一样图形化安装，又能体验到 Arch 的所有好处的一款系统。manjaro 我一直用到入学，用了一段时间感觉除了图标难看以为其他都还是不错的。显卡驱动配置起来也是很方便，但时间长了问题也来了，开机有时候会概率性的黑屏卡住，本以为找到一款完美 Linux 的我瞬间不开心了，其实 manjaro 对显卡的支持并不是很好，由于研究生研究的方向与深度学习相关需要用到 GPU，能找到一款完美支持显卡驱动的 Linux 是我当务之急，于是我放弃了 manjaro，又开始了新的探索。

## 迷茫

2021 下半年研究生入学，怀着对新学校的憧憬我来到了一个新的环境，也认识了很多朋友。大家对我使用的 Linux 也感到了些许的好奇之心，他们都在问我使用的是什么操作系统，我也热情的给他们细心的去讲解，但大家往往只是一听而过而并未做过多的深入，我也就不再往下多说。

manjaro 我是不再考虑了，每次开机玄学卡住。于是 Linux Mint 和 openSUSE 开始引起我的注意，经过使用之后发现他们极其的稳定，且都对显卡驱动支持很好。Linux Mint 是基于 Ubuntu 的发行版，使用 apt 作为包管理工具，软件的支持也很好。opensuse 是一款比较小众的 Linux，有自己独立的软件仓库，界面使用 Gnome，配置好之后非常美观，就是有一个缺点，缺包，安装一些第三方软件有时会提示缺少库文件，我也尝试过去补包但有几个始终补不上，后来就不了了之，用起了 Mint。

这段时间我也花了大量时间去美化桌面，包括 Opensuse 和 Mint。后来由于意识到花在这上面的时间太多，就不再美化了，使用 Mint 默认的原生桌面。

到了研一寒假我基本上不再搞美化了，全身心投入到技能的提高上面，因此节省出来了大量的时间可以让我配置 vim 插件以及读论文。这段时间也是我对前端感兴趣的开始。
由于本人英文很差，看论文需要翻译软件才能看得懂，而在我们研究生之间流传深广的翻译软件是一款名叫知云的翻译软件，很可惜他只能在 Windows 和 MAC 平台有才有发布，唯独忽略了我最钟爱的 Linux，这使得我不得不切换到 windows 下看论文，也十分的麻烦。之前在 github 上有位大佬写过一个全平台的翻译软件 copytranslator，由于很长时间没有维护，现在基本上在 Linux 上不能使用了，于是我萌生了自己写一款全平台的文献翻译软件，这个后续再讲，先挖个坑。

linux Mint 确实不错，包全、稳定、显卡支持好就是界面朴素了些（Mint 使用 cinnamon 桌面环境，样子和 Windows 差不多）。但不得不说它是也个很不错的 Linux 发行版，十分推荐给初学者使用 Linux（Ubuntu 我是真的不想推荐）。但后来由于想念 Gnome 桌面的那种丝滑的切换和好看的界面，我又开始蠢蠢欲动了，又想着寻找一款完美的 Linux，我梦想中的 Linux 有一下要求：

1. 系统稳定，不是滚动更新
2. 界面美观
3. 包全
4. 支持显卡驱动

## 曙光

由于实在想要一款完美的操作系统，开学之后我将 Mint 换掉了，又开始了无休止的重装系统。这段时间我锁定了 Fedora 这款 Linux，他默认的桌面系统就是 Gnome，是属于红帽系列的 rpm 包作为通用的包格式管理。印象当中红帽系列的 Linux 很稳定，很适合作为服务器来使用，这就对他有了一个刻板印象，就是一直以为红帽 Linux 的包很旧，包少。

在安装上 Fedora 上之后我发现并不是这样，相反 Fedora 的更新频率很高有很稳定，几乎满足了我对完美 Linux 的前三条。之前也有用过 Fedora，看着别人在 csdn 上写的教程尝试安装显卡驱动却都以失败告终，这次安装驱动我不再去看 csdn 了，按照 Fedora 的官方文档去安，结果居然安装成功。这正是我梦寐以求的完美 Linux，终于被我找到了。这也让我知道了看官方文档的重要性。

## 后续

后续的日子我一直在使用 Fedora，有时为了打游戏和一些必要的文档编辑需要切换到 Windows。我更愿称 Windows 为游戏系统。

现在身旁的人也在受我的影响开始玩 github 和 Linux，我也仿佛看到了当年的那个自己。