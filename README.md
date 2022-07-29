# -
利用解码芯片MT8870将电话机输出的双音频信号电话短号解调为二进制代码，再将解调出的二进制代码送单片机显示。使我们输入信号后在单片机上显示出来，连续拨号六位后，在拨第七位时单片机上显示的数据全都清零，再重新拨号。

接通电源之后，通过MT8870与一个三极管做的方向器给到单片机中断单元，再从P2.4至P2.7给到单片机。再通过字形表中的地址送到显示缓冲区再送到P0口锁存起来。利用3-8译码器的功能在P2.0-P2.2上译码使对应的数码管显示我们拨的号。使拨的号码能在显示屏上稳定的显示出来，且能在拨完6位后，再拨第七位时能清零。另一个功能是可以定时所拨号码之间的时间，所拨的两个号码之间如果超过定时的时间嘉会自动清零。

开发板我们实验室是采用STC15F2K16S2芯片的开发板。

MT8870芯片的D1、D4分别连接在开发板的P10、P13口，①处则接开发板的外部中管口，即P32口。

*有帮助请勿吝啬您的star，thanks！
