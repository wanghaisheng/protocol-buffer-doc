TimYang

Web系统通常用json来存储或者cache是非常浪费的。1条微博，用json数据结构来存所有字段(包括作者信息)，
需要5K字节左右, 用xml需要10k左右, 测试用protobuf序列化后，大约只有500字节。另外pb反序列化速度竟然比序列化速度快2倍左右，对于快速加载非常有利。


受到poppy启发，写了一个基于protobuf的轻量级RPC库，使用方式与poppy基本一致。已开源： http://github.com/BaiduPS/sofa-pbrpc



ASTA谢

数据存储的变化历程rdbms-》json-》protocol buffer       


hashjoin

上个月给Berkeley数据库代了一堂课，综述大数据，从最早的GFS/MapReduce，到Hadoop再到Spark，最后讲解了一下传统数据库系统和大数据系统的区别，以及分久必合，合久必分的局势。幻灯片刚上传到网上，和大家分享一下 Big Data Analytics Systems: What Goes Around Comes Around http://t.cn/R2ZJGSI
