# Managing Software #


----------
## rpm *[operation]* *[options]* *[file|name]*##
- **Operations**
	- **-i** 安装
	- **-e** 卸载
	- **-q** 查询一个包是否安装 若是，问询其文件包含及其他
	- **-U** 安装或更新
	- **-F, --freshen** 仅更新
	- **-V, --verify** 检查包在安装后是否被修改
	- **--rebuild** 重新编译一个*.src.rpm*源码包 RPM 4.2版本后被**`rpmbuild`**代替
	- **--rebuilddb** 重建RPM database以修错

<br/>
	
- **Options**
	- **--force** 





| Options  | Used by Operations | Description |
| ------------- | ------------- |------------- | 
|**--foece**| -i,-U,-F   |强行安装包 可能会覆盖已安软件|
|**-h,--hash**|-i,-U,-F|用#表示安装进度 |  
|**-v**|-i,-U,-F|为每个安装显示独立的[###]进度条|
|**--nodeps**|-i,-U,-F,-e| 无视包依赖 强制执行|
|**--test**|-i,-U,-F|尝试安装以发现问题 不真实安装|
|**--frefix _path_**|-i,-U,-F|指定安装目录为*path*|
|**--root** _dir_ |Any|将*dir*指定为系统根目录 救急时用|
|**-a,--all**|-q,-V|问询，检查所有的包|
|**-f** _file_<br/>**--file** _file_|-q,-V|???|
|**-p** _package_|-q|显示该rpm包的详细信息|
|**-i**|-q|显示该包详细的infomation|
|**-R,--require**|-q|显示依赖列表|
|**-l,--list**|-q|显示包中所有文件|





----------
# yum #


1. 在fedora后续版本中已被 dnf 工具取代
2. 没有**缩略格式**的命令


| Command| Description |
| ------------- | ------------- |------------- | 
| **install**|&nbsp;|
|**update**|升级所有包 配置 版本内核|
|**check-update**|检查是否有可用更新|
|**upgrade**| 升级所有包 不改变配置 版本升级 内核不变|
|**remove**<br/>**erase**|卸载软件 似**rpm -e** 但是会同时删除依赖的包|
|**list**|列出包的信息 显示是否有更新可用|
|**search**| 查找包含特定keyword的包|
|**info**|显示包信息 似**rpm -qi**|
|**clean**|清除yum的cache目录|
|**resolvedep**|显示解决某包依赖关系的包|
|**localinstall**|本地安装|
|**loccalupdate**|本地更新|
|**deplist**|显示指定包的依赖关系|