# repairLaptop
修电脑

记一次清理笔记本灰尘发生的状况-Windows自我修复无限重启
机器：华硕笔记本，出厂机械硬盘，后安装固态；系统移至固态；固态放在了原机械硬盘位置，机械硬盘放在了光驱位置。

1.正常拆机，开始敲打风扇，清除灰尘

2.装机，启动机器，开始显示Windows自动修复，修复失败，进入Windows修复选择界面；其中的还原点，cmd命令，系统恢复均尝试一遍，还是不行。

3.发现光驱位置的盘有点松，以为是这个问题，插紧光驱盘，还是不行；尝试搜索出来的  bcdEdit 命令，还是不行。

4.记得搜索出来一个说，显示的盘符和实际的不一致，我在使用还原点还原的时候也是出现了G盘，而我的系统盘是C盘，怀疑是硬盘的问题

5.把机械盘去掉，只挂固态，成功进入系统，再次插上机械盘，成功。

分析原因：
在清理灰尘完毕，没有安装固态的时候，直接启动了电脑，导致系统直接挂载了机械盘。后续再插上固态，电脑还是默认系统是在第一张盘上，所以不管怎么修复，在数据盘上怎么也不能修复出一个系统来。
在只插系统盘，启动一次，关机后再插上其他盘，再次启动就正常了。

这次清理灰尘，是因为风扇的声音很大，估计是北京的灰尘比较多，比武汉差多了。
本以为清理完后声音回小，结果还是一样的，看来是要换风扇了。
