学习笔记

重学Javascript

语言按语法分类

非形式语言

形式语言
0型 无限制文法
1型 上下文相关文法
2型 上下文无关文法
3型 正则文法

产生式(BNF)

巴科斯诺尔范式：即巴科斯范式（英语：Backus Normal Form，缩写为 BNF）是一种用于表示上下文无关文法的语言，
上下文无关文法描述了一类形式语言。它是由约翰·巴科斯（John Backus）和彼得·诺尔（Peter Naur）首先引入的用来描述计算机语言语法的符号集。

Javascript 属于上下文无关文法，表达式属于正则文法

2 ** 1 ** 2 (特例：上下文相关文法)

现代语言的特例

Python中，行首的tab符和空格会根据上一行的行首空白以一定规则被处理成虚拟终结符indent或者dedent

Javascript中， /可能是除号，也可能是正则表达式开头，处理方式类似于VB，字符串模板中也需要特殊处理}, 还有自动插入分号规则

语言的分类

形式语言 - 用途
 数据描述语言  JSON HTML XAML SQL CSS
 编程语言 C C++ Java C# Python Ruby Perl Lisp T-SQL Clojure Haskell JavaScript

形式语言 - 表达方式
 声明式语言 JSON HTML XAML SQL CSS Lisp Clojure Haskell Lisp Clojure Haskell
 命令式语言 C C++ Java C# Python Ruby Perl JavaScript

图灵完备性
 命令式  图灵机
    goto
    if while
 声明式  lambada
    递归

运行时相关概念

Statement
Grammar 简单语句 组合语句 声明
RunTime Completion Record, Lexical Environment

