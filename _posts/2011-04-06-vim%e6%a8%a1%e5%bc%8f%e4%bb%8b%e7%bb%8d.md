---
title: VIM模式介绍
author: windea
layout: post
permalink: /archives/29.html
categories:
  - VIM
---
<p style="text-align: center;">
  VIM模式介绍
</p>

Vim具有6种基本模式和5种派生模式。

### 基本模式

1.  普通模式 : 在普通模式中，用户可以执行一般的编辑器命令，比如移动光标，删除文本等等。这也是Vim启动后的默认模式。这正好和许多新用户期待的操作方式相反（大多数编辑器默认模式为插入模式）。  
    Vim强大的编辑能力中很大部分是来自于其普通模式命令。普通模式命令往往需要一个操作符结尾。例如普通模式命令&#8221;dd&#8221;删除当前行，但是第一个&#8221;d&#8221;的后面可以跟另外的移动命令来代替第二个&#8221;d&#8221;，比如用移动到下一行的&#8221;j&#8221;键就可以删除当前行和下一行。另外还可以指定命令重复次数，&#8221;2dd&#8221;（重复&#8221;dd&#8221;两次），和&#8221;dj&#8221;的效果是一样的。用户学习了各种各样的文本间移动／跳转的命令和其他的普通模式的编辑命令，并且能够灵活组合使用的话，能够比那些没有模式的编辑器更加高效的进行文本编辑。  
    在普通模式中，有很多方法可以进入插入模式。比较普通的方式是按&#8221;a&#8221;（append／追加）键或者&#8221;i&#8221;（insert／插入）键。
2.  插入模式 : 在这个模式中，大多数按键都会向文本缓冲中插入文本。大多数新用户希望文本编辑器编辑过程中一直保持这个模式。  
    在插入模式中，可以按ESC键回到普通模式。
3.  可视模式 : 这个模式与普通模式比较相似。但是移动命令会扩大高亮的文本区域。高亮区域可以是字符、行或者是一块文本。当执行一个非移动命令时，命令会被执行到这块高亮的区域上。Vim的&#8221;文本对象&#8221;也能和移动命令一样用在这个模式中。
4.  选择模式 : 这个模式和无模式编辑器的行为比较相似（Windows标准文本控件的方式）。这个模式中，可以用鼠标或者光标键高亮选择文本，不过输入任何字符的话，Vim会用这个字符替换选择的高亮文本块，并且自动进入插入模式。
5.  命令行模式 : 在命令行模式中可以输入会被解释成并执行的文本。例如执行命令（&#8221;:&#8221;键），搜索（&#8221;/&#8221;和&#8221;?&#8221;键）或者过滤命令（&#8221;!&#8221;键）。在命令执行之后，Vim返回到命令行模式之前的模式，通常是普通模式。
6.  Ex模式 : 这和命令行模式比较相似，在使用&#8221;:visual&#8221;命令离开Ex模式前，可以一次执行多条命令。

### 演生模式

1.  操作符等待模式 : 这个派生模式指普通模式中，执行一个操作命令后Vim等待一个&#8221;动作&#8221;来完成这个命令。Vim也支持在操作符等待模式中使用&#8221;文本对象&#8221;作为动作，包括&#8221;aw&#8221;一个单词（a word）、&#8221;as&#8221;一个句子（a sentence）、&#8221;ap&#8221;一个段落（a paragraph）等等。  
    比如，在普通模式下&#8221;d2as&#8221;删除当前和下一个句子。在可视模式下&#8221;apU&#8221;把当前段落所有字母大写。
2.  插入普通模式 : 这个模式是在插入模式下按下ctrl-o键的时候进入。这个时候暂时进入普通模式，执行完一个命令之后，Vim返回插入模式
3.  插入可视模式 : 这个模式是在插入模式下按下ctrl-o键并且开始一个可视选择的时候开始。在可视区域选择取消的时候，Vim返回插入模式。
4.  插入选择模式 : 通常这个模式由插入模式下鼠标拖拽或者shift方向键来进入。当选择区域取消的时候，Vim返回插入模式。
5.  替换模式 : 这是一个特殊的插入模式，在这个模式中可以做和插入模式一样的操作，但是每个输入的字符都会覆盖文本缓冲中已经存在的字符。在普通模式下按&#8221;R&#8221;键进入。

&nbsp;