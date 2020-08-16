学习笔记
浏览器工作原理

做一个 toy Browser

HTTP基础

URL - http -> HTML - parse -> DOM - css computing -> DOM with CSS - layout -> DOM with position - render -> Bitmap

parse，把HTML变成DOM树， CSS computing。  得到一棵带CSS属性的DOM树(DOM with CSS)。 layou(布局，排版)

有限状态机处理字符串：

(状态机)

每一个状态都是一个机器

每一个机器都知道下一个状态
    每个机器都有确定的下一个状态 (Moore)
    每个机器根据输入决定下一个状态 (Mealy)

有限状态机里每一个机器都是解耦的。

JS中的有限状态机 (Mealy)

使用状态机处理字符串

HTTP请求

ISO-OIS 七层网络模型

HTTP -- require('http')
TCP  -- require('net')
Internet
4G/5G/Wi-Fi

TCP与IP的一些基础知识

流
包
端口
IP地址
require('net');
libnet/libpcap



