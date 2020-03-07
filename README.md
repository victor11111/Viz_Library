# Viz_Library
VTK7.1.1和OPENCV3.4.1_Viz编译好的库（可以直接使用）

#编译过程可以参考我的CSDN博客
https://blog.csdn.net/qq_36638362/article/details/104711920

#编译过程
//编译VTK//////////////////////////////
//configure
BUILD_SHARED_LIBS	//lib勾选
BUILD_EXAMPLES	//例子勾选
CMAKE_DEBUG_POSTFIX	_d	//debug后缀_d release无后缀
CMAKE_INSTALL_PREFIX	//VTK安装目录(D:/VTK-8.2.0/VTK-install)分隔符都需要使用"/"，而不能使用windows的"\"
//Generate
//管理员权限打开VS2017后，再打开项目VTK.sln。
//选择Debug与x64，然后右键ALL_BUILD，点击生成
//再右键INSTALL，选择仅用于项目–>仅生成INSTALL
install好，添加环境变量！

//vtk8.2.0编译过程中会出现错误
//C2065	“__func__”: 未声明的标识符



//编译viz///////////////////////////////////
VTK_DIR		//install VTK的位置，会默认，检查（D:/program files/Opencv_vtk/VTK-8.2.0/VTK/Release/lib/cmake/vtk-8.2）
WITH_VTK	//勾选
BUILD_opencv_viz		//勾选
BUILD_opencv_world		//勾选
CMAKE_DEBUG_POSTFIX	_d	//debug后缀_d release无后缀
CMAKE_INSTALL_PREFIX	//install目录
