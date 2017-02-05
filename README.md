# javamail-cracked
base on java mail library and cracked for receiving 163/qq mail

## 网易邮箱的问题
如果你在尝试基于javamail使用IMAP协议接收网易邮箱（163/126/yeah）的邮件，多半会发现，网易会阻止客户端的连接。    
有时候会发送一封邮件让邮箱所有者确认，有时候却没有，导致无法稳定的接收，但使用foxmail却没有这样的问题。  
原因是网易对IMAP协议进行了修改，需要按照他的规则发送指令才能正常接收，因此对javamail的源代码进行了简单的crack，伪装成一个foxmail客户端，实现正常的接收。   

## QQ邮箱的问题
QQ邮箱使用javamail的getMessagesByUID方法收取邮件也会失败，同样是发送指令的问题，进行了修改