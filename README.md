____ _ ____
| _ \ ___ _ __| |_/ ___| ___ __ _ _ __ ___ _ __
| |_) / _ \| '__| __\___ \ / __/ _` | '_ \ / _ \ '__|
| __/ (_) | | | |_ ___) | (_| (_| | | | | __/ |
|_| \___/|_| \__|____/ \___\__,_|_| |_|\___|_| v5.0

1、此程序需要在cmd中以命令的方式加载参数来运行。

2、程序可将url地址转换为IP地址进行扫描，所有url地址必须以 http:// 开头也可以是 https:// 否则程序无法转换。

3、可以把要扫描的多个“IP”以每行一个的形式 或者 某个“IP段”放入与程序同目录下的ip.txt中，程序会自动读取文件开始扫描。

4、程序内置了50、100、500三个范围的常见端口，默认为扫描500个常见端口。也就是说 --top 参数可以填写50或者100或者500，此参数优先，如果使用此参数则无法指定扫描端口范围。与下一项互斥。

5、如果想扫描端口范围，就无需top参数，需要输入起始端口与结束端口， --start_port 100 --end_port 9000

6、如果想设置线程，可以使用--thread_num 8   来指定用多少个线程开始扫描，线程越多扫描的越快，但是需要根据自己的电脑配置、网速来，不要设置太多。

7、程序扫描完毕会有提示，且结果会保存在同目录下，生成jieguo.csv文件

程序还可进行各种设置，如扫描指定的端口范围等，具体使用方法假定此程序名称为"portscaner.exe"给出示例如下：


 

[参数说明]

/*表示以8个线程，扫描指定IP常见的100个端口*/

portscaner --thread_num 8 --top 100


/*表示以10个线程(当不设置某个参数时会使用默认值进行扫描)，扫描指定IP 100到9000的所有端口*/

portscaner --start_port 100 --end_port 9000

/*表示以10个线程，扫描指定IP常见的500个端口*/

portscaner
 

[ip.txt说明]
ip 192.168.1.1-192.168.2.255 or 192.168.1.3


下载地址：https://github.com/sysalong/portscaner/releases/download/v5.1/default.zip
 

ip.txt内容为示例，请换成自己需要扫描的，可以是一个或是多个。

如果软件报毒，请加白名单，因为加了压缩壳导致。
