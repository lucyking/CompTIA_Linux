
## File Archining Commands ##

### tar&nbsp;&nbsp;[options]&nbsp;&nbsp;[files]###
>**tar.gz[2]** == **tgz[2]**

----------

 - **Commands 命令**
 	- **x** ,--extract,--get  解压 
 		- tar ***xzf*** tarball.tar.gz
 	- **c** ,--create 创建          
 		- tar ***czf*** tarball.tar.gz *.png
 	- **u** ,--update         添加未包含的tar文件
 	- **t** ,--list			  列出压缩包内文件内容
 	- **d** ,--diff,--compare 
	- **r** ,--append     添加普通文件至压缩包
	- **A** ,--concatena  添加tar至压缩包
	- 

----------

 - **Qualifier 修饰符**
 	- **C** ,--directory *dir* 在解压前，先移动到*dir*目录里
 	- **f** &nbsp;,--file *[host:]file* 指定要解压的文件
 	- **v** ,--verbose 
 	- **z** ,--gzip,--ungzip
 		- tar ***zxvf***  &nbsp;* tarball.tar.gz 
 		- ***`gunzip -c tarball.tar.gz | tar xvf`*** 
 	- **j** ,--bzip2
 		- tar ***jxvf***  &nbsp;tarball.tar.gz2



----------

