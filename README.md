IAP_Load
========

STM32 IAP升级工具

使用前，先用keil的fromelf将axf转换成bin文件。
载入bin文件并打开串口，按下载就可以了。

工具将Bin文件，以1K为单位分块传送。传送最后不足1K的数据，将补全0xff至1K。

> 传输格式为 

> data_len_L  data_len_H  data(no more than 1K)   index_L index_H CRC

> 2B数据长度

> 最多1KB的有效数据（真正的烧录数据）

> 2B的数据索引（表示接收/发送的数据是第几个1K）

> 4B CRC（预留）


     -------------------------040902---广技师---校本部------------------------------
