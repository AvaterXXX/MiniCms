# Authentication Vulnerability
---------------------------
The problem code is in mc-admin/post.php
![](https://github.com/AvaterXXX/MiniCms/blob/master/image/%E8%B6%8A%E6%9D%831.png)

There are a lot of things here but it doesn't matter, let's take a look at the permission verification
According to the analysis of the source code, the CMS's permission authentication is in `mc-admin/head.php`
![](https://github.com/AvaterXXX/MiniCms/blob/master/image/%E8%B6%8A%E6%9D%832.png)

The page was called in `mc-admin/post.php` , but it is in line 188.
![](https://github.com/AvaterXXX/MiniCms/blob/master/image/%E8%B6%8A%E6%9D%833.png)

In other words, we have already made the delete operation before the permission verification, so there is an unauthorized violation
Let's get the ID of the article first
![](https://github.com/AvaterXXX/MiniCms/blob/master/image/%E8%B6%8A%E6%9D%834.png)

Constructing a POC `/mc-admin/post.php?delete=qe54cn&state=delete` Visit again and found that it has been deleted
![](https://github.com/AvaterXXX/MiniCms/blob/master/image/%E8%B6%8A%E6%9D%835.png)


#  Information Exposure
---------------------------
![](https://github.com/AvaterXXX/MiniCms/blob/master/image/%E8%B6%8A%E6%9D%835.png)
According to the previous operation, you can see that the path information is leaked. Here, you do not need to log in
