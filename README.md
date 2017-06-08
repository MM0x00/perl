# perl 在线实验环境

## 软件简介

软件基本信息，License，所属的类别，作用，特点等。

Perl，一种功能丰富的计算机程序语言，运行在超过100种计算机平台上，适用广泛，从大型机到便携设备，从快速原型创建到大规模可扩展开发。[1] 
Perl最初的设计者为拉里·沃尔（Larry Wall），于1987年12月18日发表。现在的版本为Perl 6，于2015年12月25日更新。
Perl借取了C、sed、awk、shell 脚本语言以及很多其他程序语言的特性，其中最重要的特性是它内部集成了正则表达式的功能，以及巨大的第三方代码库CPAN。简而言之，Perl像C一样强大，像awk、sed等脚本描述语言一样方便，被Perl语言爱好者称之为“一种拥有各种语言功能的梦幻脚本语言”、“Unix 中的王牌工具”。
Perl 一般被称为“实用报表提取语言”（Practical Extraction and Report Language），你也可能看到“perl”，所有的字母都是小写的。一般，“Perl”，有大写的 P，是指语言本身，而“perl”，小写的 p，是指程序运行的解释器。

所属类别是编程语言

特点：

1.免费软件

2.容易移植

3.方便简洁，易于操作

## 软件官网

https://www.perl.org/

## Dockerfile 使用方法

Dockerfile在您的Perl应用程序项目中创建一个
```
FROM perl:5.20

COPY . /usr/src/myapp

WORKDIR /usr/src/myapp

CMD [ "perl", "./your-daemon-or-script.pl" ]
```
然后，构建并运行Docker映像：
```
$ docker build -t my-perl-app .
$ docker run -it --rm --name my-running-app my-perl-app
```
运行一个Perl脚本

对于许多简单的单个文件项目，您可能会发现编写完整的不方便Dockerfile。在这种情况下，您可以直接使用Perl Docker映像运行Perl脚本：
```
$ docker run -it --rm --name my-running-script -v "$PWD":/usr/src/myapp -w /usr/src/myapp perl:5.20 perl your-daemon-or-script.pl
```
## 资源链接

- https://www.perl.org/
