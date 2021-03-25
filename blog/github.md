访问 github 老是连接超时，工作需要下载的文件都在这里，无奈，只好百度解决问题，终于在CSDN找到了一篇博客。

(*老是审核不通过，无奈只能这样换成图片，见谅)

一，错误分析： 怀疑连接不到 最大的代码开源平台，在cmd窗口中，尝试ping一下百度。

![logo](../_media/01.png ':size=993x519')  
 说明网络连接正常。

二，然后再 ping一下github·com 
C:\Users\Bai>ping github.com 
正在 Ping github . com 【 1 11 . 13 . 100 . 91 』 具有 32 字节的数据：请求超时。请求超时。请求超时。请求超时。 1 11 . 1 3 . 100 . 91 的 Ping 统计信息：数据包：已发送二 4 ，已接收二 0 ，丢失二 4 ( 1 00 ％丢失） , 确实 Ping 不通。因此怀疑是：本地 0NS 无法解析导致的。
![logo](../_media/02.png ':size=714x501')  

三，错误解决 打开C:\Windows\System32\drivers\etc\hosts，内容如下：

![logo](../_media/03.png ':size=703x398') 

![logo](../_media/04.png ':size=498x152') 

![logo](../_media/05.png ':size=673x473') 

重启cmd 窗口 ，ping 一下 

![logo](../_media/06.png ':size=981x512') 

至此，问题解决。

原文链接：

blog.csdn.net/mybookln_nl… （感谢大佬）

blog.csdn.net/hanchao5272…

特别注意：另外Win10无法直接保存hosts，参见下面链接：

jingyan.baidu.com/article/624…