# cmake最低版本需求，不加会有警告信息
CMAKE_MINIMUM_REQUIRED(VERSION 2.6)

PROJECT(HELLO) 		# 项目名称

# 把当前目录(.)下所有源代码文件和头文件存放到变量SRC_LIST中
AUX_SOURCE_DIRECTORY(. SRC_LIST)

# 生成应用程序 hello（elf文件） (windows下自动生成hello.exe) 。
ADD_EXECUTABLE(hello ${SRC_LIST})  #使用${}方式来取得变量中的值
//add_executable(hello main.c)    # 指令不区分大小写
