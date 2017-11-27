<p>
    ＃公里
</p>
<p>
    测试用
</p>
<p>
    vlmcsd转载源码
</p>
<p>
    binaries文件下各个版本的kms服务器文件
</p>
<p>
    使用方法
</p>
<p>
    linux
</p>
<p>
    下载源代码
</p>
<p>
    yum install git
</p>
<p>
    git clone https://github.com/livefwq/kms.git
</p>
<p>
    进入binaries 文件夹
</p>
<p>
    cd kms/binaries
</p>
<p>
    选择你系统需要的版本（以centos为例子intel cpu为例子 64位系统）
</p>
<p>
    cd Linux/intel/glibc/
</p>
<p>
    chmod 777 vlmcsd-x64-glibc
</p>
<p>
    mv vlmcsd-x64-glibc kms
</p>
<p>
    cp kms /root/
</p>
<p>
    ./kms
</p>
<p>
    此时kms激活服务器已经启动
</p>
<p>
    添加开机启动
</p>
<p>
    &nbsp;vi /etc/rc.local
</p>
<p>
    &nbsp;最后加入
</p>
<p>
    &nbsp;/root/kms
</p>
<p>
    &nbsp;保存退出
</p>
<p>
    &nbsp;
</p>
<p>
    &nbsp;添加进程守护
</p>
<p>
    &nbsp;crontab -e
</p>
<p>
    加入这一行
</p>
<p>
    */5 * * * * /root/kms
</p>
<p>
    <br/>
</p>
<p>
    <br/>
</p>
<p>
    <br/>
</p>
<p>
    端口被占用
</p>
<p>
    lsof -i :1688
</p>
<p>
    或者
</p>
<p>
    netstat -lnp|awk &#39;BEGIN{prt=&quot;:1688$&quot;}{if ($4 ~ prt) print $0}&#39;
</p>
<p>
    结束这进程 （PID填你看到的）
</p>
<p>
    kill -9 PID
</p>
<p>
    <br/>
</p>
<p>
    <br/>
</p>
<p>
    <br/>
</p>
