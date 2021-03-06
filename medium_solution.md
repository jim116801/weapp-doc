# 单机版架构升级

![单机版架构图](https://mc.qcloudimg.com/static/img/7d40df0347cbfad83c16a011a435271c/24.png)

如果您在使用小程序云资源过程中发现现有配置不能满足您的业务需求，您可以选择升级云服务器和云数据库的配置。

- 云服务器 CVM 提供带宽、CPU、内存、磁盘等配置的升级
- 云数据库 CDB 提供内存、硬盘的升级

## 云服务器配置升级
首先需要登录[腾讯云CVM控制台](https://console.qcloud.com/cvm)

### 升级CPU和内存

>只有<font color="red">**关机状态**</font>下的，<font color="red">**系统盘与数据盘均为云盘**</font>的CVM实例可以调整配置。

1) 对于要调整配置的关机CVM实例，在右侧操作栏，点击【更多】-【云主机设置】-【调整配置】。

2) 在调整配置弹出框中，选择升级后的配置，完成支付或确认后即可即时调整主机配置。

![调整配置](https://mc.qcloudimg.com/static/img/fe9f8398edcb067e2a300de63418eeea/2.png)

### 调整CVM磁盘配置

>只有<font color="red">**关机状态**</font>下的，<font color="red">**数据盘为云盘**</font>的CVM实例可以调整磁盘。
>如果您的云服务器还没有数据盘，可以先购买弹性云盘后进行挂载，<font color="red">**注意购买的云盘必须与要挂载的云服务器同地域同可用区**</font>，见具体[操作文档](https://www.qcloud.com/doc/product/362/2922)，

1) 对于要调整配置的关机CVM实例，在右侧操作栏，点击【更多】-【云主机设置】-【调整磁盘】

2) 选择需要调整的磁盘

![选择云盘](https://mc.qcloudimg.com/static/img/b085b0259bade00f6277b359c3f779c7/3.png)

3) 在调整磁盘弹出框中，选择调整后的磁盘大小（不可低于当前磁盘大小），完成支付后即时调整主机磁盘大小，调整后的磁盘需要手动挂载才可使用。

![调整磁盘](https://mc.qcloudimg.com/static/img/e30855318f8bef937cdc035b83c30dc5/4.png)

### 调整网络

对于要调整配置的关机CVM实例，在右侧操作栏，点击【更多】-【云主机设置】-【调整网络】。

![调整网络](https://mc.qcloudimg.com/static/img/5c4143697880b932891548732ab12ae8/1.png)

## 云数据库配置升级
>升级过程中，是不能取消本次升级操作的。

登录[云数据库管理控制台](https://console.qcloud.com/cdb)，可通过“升级”操作升级指定实例的实例规格。
![升级](https://mc.qcloudimg.com/static/img/0056b6d5165e0afe240763963a302bf3/5.png)

### 注意事项

1.实例升级过程中原实例的正常使用将不受影响，如数据的导入、导出功能。

2.升级前后实例的名称、访问IP、访问端口均不发生变化。

**3.升级完成时会产生秒级的MySQL数据库连接断开，建议程序有自动重连功能。**

**4.在升级过程中，请尽量避免修改MySQL的全局参数、实例名称、用户密码等操作。**