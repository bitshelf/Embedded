![image-20200424185023708](/home/ljz/.config/Typora/typora-user-images/image-20200424185023708.png)

###  C++11对C++03的增强，或者说C++11的“Modern”的特点之一就是由auto和decltype构成的自动类型推导系统。

 

#### 但是，auto与初始化列表结合，又有一些坑。你在写代码时如果经常将auto与列表初始化一起使用，那么会遇到一些问题。本节只介绍auto的常见用法。auto与初始化列表结合的坑，得由你自己去踩了。



#### 为了说明auto有多么复杂，这里摘取 https://cppreference.com 网站列出的auto的语法格式：

 

|         **auto** ***variable\*** ***initializer\***          | **(1)** | **(C++11** **起****)** |
| :----------------------------------------------------------: | ------- | ---------------------- |
|      **auto** ***function\*** **->** ***return type\***      | (2)     | (C++11 起)             |
|                   **auto** ***function\***                   | (3)     | (C++14  起)            |
| **decltype****(****auto****)** ***variable\*** ***initializer\*** | (4)     | (C++14 起)             |
|              **decltype**(**auto**)function\***              | (5)     | (C++14  起)            |
|                        **auto** `::`                         | (6)     | (概念 TS)              |
| ***cv\****(****可选****)** **auto** ***ref\*****(****可选****)** ***parameter\*** | (7)     | (C++14  起)            |
|         `template` `<` **auto** ***Parameter\*** `>`         | (8)     | (C++17 起)             |
| ***cv\*****(****可选****)** **auto** ***ref\*****(****可选****)** `[` ***identifier-list\*** `]` ***initializer\*** `;` | (9)     | (C++17  起)            |