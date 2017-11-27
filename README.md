＃公里
测试用
vlmcsd转载源码
binaries 文件下各个版本的kms服务器文件
使用方法
linux
下载源代码
yum install git
git clone https://github.com/livefwq/kms.git
进入binaries 文件夹
cd kms/binaries
选择你系统需要的版本（以centos为例子intel cpu为例子 64位系统）
cd Linux/intel/glibc/
chmod 777 vlmcsd-x64-glibc
mv vlmcsd-x64-glibc kms
cp kms /root/
./kms
此时kms激活服务器已经启动


添加开机启动
 vi /etc/rc.local
 最后加入
 /root/kms
 保存退出
 
 添加进程守护
 crontab -e
加入这一行
*/5 * * * * /root/kms



端口被占用
lsof -i :1688
或者
netstat -lnp|awk 'BEGIN{prt=":1688$"}{if ($4 ~ prt) print $0}'
结束这进程 （PID填你看到的）
kill -9 PID



