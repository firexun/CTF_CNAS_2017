# 3 Hints

## First Hints
6.数据完整性 提示1：存在index.jsp.bak,代码泄露，RSA基础，由e，p，q算出d，m可爆破。 10.综合题 提示1：zip文件里是ssh私钥文件，服务器上只存在一个文件。

## Second Hints
1.身份鉴别 提示1：根目录下有个robots.txt文件，里面有后台地址，密码是admin的弱口令 2.log目录下的日志文件里有个apk，apk逆向分析，异或算法得到flag

## Third Hints
10题：综合题 关键函数 sub_4012D0,IDA和结合算法扫描工具，可以确定算法是 RC5 加密 程序进行了四次加密，每次加密8个字节，每次使用的key不同，通过动态调试可以获取到对应的key，采用的16轮加密后的数据异或0x11之后与固定字符串比较。