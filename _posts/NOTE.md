1.liunx编译过程:
				
			C语言   .c    ---> .exe ?

			几个过程:
			
			-E 预处理:把.h .c展开形成一个文件。宏定义直接替换 头文件 库文件 .i
		  gcc -E hello.c -o hello.i

			-S 汇编:   .i 生成一个汇编代码文件  .s
		  gcc -S hello.i -o hello.s

			-c 编译:    .s 生成一个  .o .obj
		  gcc -c hello.s -o hello.o

			-o 链接:   .o 链接  .exe(window) .elf(liunx)
		  gcc  hello.o -o hello

2.liunx命令:
			
			tar

			tar是liunx中最常用的解压命令。tar命令可以用于处理后缀名为tar，tar.gz,tgz,.tar.Z,tar.bz2的文件。
			涉及参数说明:

			| -c  | 建立新的压缩文件          |
			| -r  | 添加文件到已经压缩的文件  |
			| -v  | 显示操作过程              |
			| -x  | 从压缩的文件中提取文件    |
			| -f  | 指定压缩文件              |		
			

			chmod

			一、访问权限

			访问权限分为读(read)、写(write)、执行(execute)三种，并且涉及到文件的所有者(user)、文件所属组(group)、其他人(other)三个主体。

			drwxr-xr-x

			-rw-r--r--

			第一位文件类型
			常见的有普通文件，目录，字符设备文件，块设备文件，符号链接文件:

			- :普通文件用touch <file name>创建
			-d:目录文件(directory)，可用mkdir <dir-name>创建
			-c:字符串文件，如路由器设备
			-b:块设备文件(block),如硬盘，光驱等
			-I:符号链接文件(link)

			| 第二～四位 | 第五～七位 | 第八～十位 |
			| user       | group      | other      |

			r:(4) read
			w:(2) writer
			x:(1) execute
			-:表示无权限


			文件(file)是一块储存信息的储存器区域

			流(stream)是一个理想化的数据流，实际输入或输出映射到这个数据流

			EOF(end of file，文件尾)
			通常EOF在stdio.h文件中定义，如下所示

			#define EOF -1

			函数(function)是用于完成特定任务的程序代码的自包单元




