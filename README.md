# rtksingle
基于rtklib2.4.2中rnx2rtkp功能的VS2019控制台工程，用于学习文件流、数据流和解算算法

## 2021.3.21
加入了测试数据文件夹< datas >，可得到单点定位结果，用于测试代码逻辑。

运行时rtksingle.vcxproj.user文件中命令参数要对应的测试数据，
在VS中的修改方法是“调试-> rtksingle的调试属性 -> 配置属性 -> 调试 -> 命令参数 / 工作目录 ”
命令参数应为
-k opts1.conf -o singlepos.txt hksl0670.20o brdc0670.20n
工作目录应为
$(ProjectDir)\datas 
数据有以下文件
< datas >
--  < brdc0670.20n >    武汉IGS数据中心下载http://www.igs.gnsswhu.cn/
--  < hksl0670.20o >    武汉IGS数据中心下载http://www.igs.gnsswhu.cn/
--  < opts1.conf >      RTKlib文件夹 ...\rtklib_2.4.2\rtklib_2.4.2\app\rnx2rtkp\gcc\opts1.conf
--  < singlepos.txt >   调试结果，自动生成
