# Command Execution
-----------------------
Write payload at the site title
![](https://github.com/AvaterXXX/MiniCms/blob/master/image/%E5%91%BD%E4%BB%A4%E6%89%A7%E8%A1%8C1.png)
The var_export function is used here
![](https://github.com/AvaterXXX/MiniCms/blob/master/image/%E5%91%BD%E4%BB%A4%E6%89%A7%E8%A1%8C2.png)
The htmlspecialchars function is used below, but this function does not affect our command execution, so there is no need to consider
![](https://github.com/AvaterXXX/MiniCms/blob/master/image/%E5%91%BD%E4%BB%A4%E6%89%A7%E8%A1%8C3.png)
As you can see from the previous screenshot, because var_export is used, there is no escape here. Can you really order execution?
The answer is definitely yes, but it is in install.php
![](https://github.com/AvaterXXX/MiniCms/blob/master/image/%E5%91%BD%E4%BB%A4%E6%89%A7%E8%A1%8C4.png)

You can see that there is no filtering here, and the POST data is directly stored in the configuration file, thus causing the command execution or GETCHELL

![](https://github.com/AvaterXXX/MiniCms/blob/master/image/%E5%91%BD%E4%BB%A4%E6%89%A7%E8%A1%8C5.png)
![](https://github.com/AvaterXXX/MiniCms/blob/master/image/%E5%91%BD%E4%BB%A4%E6%89%A7%E8%A1%8C6.png)
