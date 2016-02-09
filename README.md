# UDP_IM
一个简单的即时通讯工具，包括服务器端和客户端程序，只能在Linux下运行。

程序分为聊天记录，输入框，其他在线用户三部分。聊天记录不能翻页。<br />
**程序使用一个16字节的ID（输入的ID过长会自动截取前16字节）唯一标识一个在线用户，客户端异常退出会导致该ID不能再次被使用。**<br />
**由于最多只能发送29个用户的ID，所以服务器端限制只能同时有29个用户在线。**<br />
**客户端允许的操作只有四种：上下左右选择要发送消息的目标用户。Ctrl-C正常退出。回车键发送消息。其他任何输入会全部显示（如果能显示）在输入框内。**<br />
**没有真正的图形界面，受Rougelike RPG启发，使用ncurses库作为图形界面，其中使用了菜单模拟其他在线用户列表。**<br />
**程序使用UDP 8888端口通信。**<br />
经测试，在ubuntu 15.10下运行正常，偶尔可能由于清屏引起屏幕乱码，没能很好解决，但不影响使用，继续输入就会恢复正常。

程序依赖
---
**程序的语言支持跟随系统，但对unicode支持很不好，尽可能只使用英文。**<br />
**需要安装ncurses库。** 可以通过GNU的FTP目录：http://www.gnu.org/order/ftp.html 找到提供免费下载NCURSES文件包的站点。

安装
---
已经包含了Makefile，生成的可执行文件会在**exe/**目录下。
