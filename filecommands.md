## File Commands ##

### ls&nbsp;&nbsp;[options]&nbsp;&nbsp;[files]###
1. **list** 的缩写
2. 可以同时显示多个目录: ***ls dir1/ dir2/ dir3/*** 

- **options**
	- **-a,--all** 显示包含隐藏文件（*.filename*）内的所有文件
	- **--color**&nbsp;用不同颜色显示目录，链接等
	- **-d,--directory** 仅显示目录名 不显示其包含文件
	- **-l** 显示权限+所有者+组+文件大小+创建时间
	- **-F,--file-type** 添加文件类型后缀:
		- **/** &nbsp;&nbsp;&nbsp; 目录
		- **@** &nbsp;&nbsp;链接   
		- **=**&nbsp;&nbsp;&nbsp; Socket
		- **|**  &nbsp;&nbsp;&nbsp;  Pipe

<br/>
----------

### cp&nbsp;&nbsp;[options]&nbsp;&nbsp;*source*&nbsp; *destination*###
> 1. 当复制到目录时 若没有指定新文件名 则沿用旧文件名
> 2. 复制的文件默认属于当前用户

- **options**<br/>
	- **-f,--force** 直接覆盖同名旧文件
	- **-i,--interactive** 覆盖前问询
	- **-p,--preserve**  保持原来的文件owner和permission属性
	- **-R,--recursive** 递归复制子目录 创建特殊文件 
 		- -r将特殊的FIFO Pipe cdev文件当做普通文件复制
 		- -R重新创建特殊文件
	- **-u,--update** 当目标文件__较旧__或__不存在__时复制文件
	
	 
<br/>
----------
### mv&nbsp;&nbsp;[options]&nbsp;&nbsp;*source*&nbsp; *destination*###
 1.**不同的filesystem之间不能移动文件**<br/>
 2.**在同一分区或磁盘中mv只是改变目录结构 无需移动 很快**<br/>
 3.**不同分区或磁盘中移动需要读取、写入、删除旧文件 很慢**<br/>




<br/>
----------
<br/>

### rm&nbsp;&nbsp;[options]&nbsp;&nbsp;*files*###
 - **-r,-R,--recursive** 递归移除子目录
 - **-d,--dir** 移除空目录

<br/>
----------
<br/>
<br/>
<br/>

### touch&nbsp;&nbsp;[options]&nbsp;&nbsp;*files*###
>**make编译根据timestamp的新旧来判断哪些文件被更新和需要重新编译**


-  **File Timestamp:**
	- modification time
	- change time
	- access time

	默认情况下touch改变 **`modified time`** 和 **`change time`**
- **options**
	- **-a,--time=atime** 仅修改**`access time`**
	- **-m,--time=mtime** 仅修改**`modified time`**
	- **-c,--no-create**  &nbsp;不新建文件
	- **-t** &nbsp;&nbsp;_timestamp_ 修改时间戳 
		- *timestamp*: **`MMDDhhmm[[CC]YY][.ss]`** 
			- *eg:*`02292300[20]09.59` > `2009/02/29 23:00:59`   <br/>
	- **-f** _reffile_,**--refference**=*reffile* 复制目标文件的时间戳   