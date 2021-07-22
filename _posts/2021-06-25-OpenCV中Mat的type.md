---
layout: post
title: "OpenCV中Mat的type"
date: 2021-06-25 17:00:00
categories: [opencv]
published: true
comments: false
copyright: true
original: true
reprintAuthor:
reprintUrl:
permalink: 
---

opencv中Mat存在各种类型，其中mat有一个type()的函数可以返回该Mat的类型。
类型表示了矩阵中元素的类型以及矩阵的通道个数，它是一系列的预定义的常量，
其命名规则为CV_(位数）+（数据类型）+（通道数）。具体的有以下值： 

![](https://abaoa.cn/assets/post/2021-06-25-17-00-00/MatType.png)

1. Unsigned 

8bits(一般的图像文件格式使用的大小)
IplImage数据结构参数：IPL_DEPTH_8U
CvMat数据结构参数：CV_8UC1，CV_8UC2，CV_8UC3，CV_8UC4

 
变量类型	空间大小	范围	其他
uchar	8bits	0~255	(OpenCV缺省变量,同等unsigned char)
unsigned char	8bits	0~255
 

2. Signed 8bits
IplImage数据结构参数：IPL_DEPTH_8S
CvMat数据结构参数：CV_8SC1，CV_8SC2，CV_8SC3，CV_8SC4

变量类型	空间大小	范围	其他
char	8bits	-128~127
3. Unsigned 16bits

IplImage数据结构参数：IPL_DEPTH_16U

CvMat数据结构参数：CV_16UC1，CV_16UC2，CV_16UC3，CV_16UC4

变量类型	空间大小	范围	其他
ushort	16bits	0~65535	(OpenCV缺省变量,同等unsigned short int)
unsigned short int	16bits	0~65535	(unsigned short)
 
4. Signed 16bits

IplImage数据结构参数：IPL_DEPTH_16S

CvMat数据结构参数：CV_16SC1，CV_16SC2，CV_16SC3，CV_16SC4

变量类型	空间大小	范围	其他
short int	16bits	-32768~32767	(short)
 

5. Signed 32bits IplImage数据结构参数：

IPL_DEPTH_32S

CvMat数据结构参数：CV_32SC1，CV_32SC2，CV_32SC3，CV_32SC4

变量类型	空间大小	范围	其他
int	32bits	-2147483648~2147483647	(long)
6. Float 32bits

IplImage数据结构参数：IPL_DEPTH_32F

CvMat数据结构参数：CV_32FC1，CV_32FC2，CV_32FC3，CV_32FC4

变量类型	空间大小	范围	其他
float	32bits	1.18*10-38~3.40*1038	 
7. Double 64bits

CvMat数据结构参数：CV_64FC1，CV_64FC2，CV_64FC3，CV_64FC4

变量类型	空间大小	范围	其他
double	64bits	2.23*10-308~1.79*10308	 
 

8. Unsigned 1bit

IplImage数据结构参数：IPL_DEPTH_1U

变量类型	空间大小	范围	其他
bool	1bit	0~1	 
