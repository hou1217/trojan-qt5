## Trojan-Qt5
官网地址:
<https://portal.shadowsocks.nz/>
下载地址：
<https://dl.trojan-cdn.com/trojan/>
配置地址：
<https://portal.shadowsocks.nz/knowledgebase/161/>

## 【Windows】Trojan-QT5 设置方法
* 本文截图、导入配置文件对应 V0.0.9 版本客户端（帮助 > 关于 查看客户端版本号）
* 由于部分客户端版本存在配置互不兼容的情况，建议更换版本时请删除之前的版本重新进行配置
* 目前客户端流量统计功能无法正常工作，显示用量 0 是正常的
* 教程对应的服务版本为： Lite / Pro 服务
* 请注意在 1.0 以上版本中，客户端的 socks5 的默认端口已不再是 1080 ，请前往 设置 > 常规设置 > 入站设置 进行查看。
### 1. 下载客户端
访问右侧的链接下载 Trojan-Qt5-Windows.[版本号].zip 文件：<https://dl.trojan-cdn.com/trojan/>

* 如出现 VCRUNTIME140.dll 和 MSVCP140.dll 缺失,需点击以下链接安装 Visual C++ redistributable packages for Visual Studio 2015, 2017 and 2019
x86: [vc_redist.x86.exe](https://aka.ms/vs/16/release/vc_redist.x86.exe)
x64: [vc_redist.x64.exe](https://aka.ms/vs/16/release/vc_redist.x64.exe)
* 如果点击连接时时闪退/报错/没有反应，请确认没有其他程序占用客户端的监听端口，建议将其他代理客户端退出后试试
### 2. 查看节点信息
登入到客户中心，依次访问 产品服务 > [我的产品与服务](https://portal.shadowsocks.nz/clientarea.php?action=products) ，查看 Trojan 服务对应的 云加速服务 - Lite / Pro 服务器信息。

### 3. 添加节点
添加方式支持
手动(3.1)
导入配置文件(3.2) 
扫码(3.3)

也通过订阅链接进行添加： 通过订阅链接添加节点 [Trojan-QT5 / Shadowrocket](https://portal.shadowsocks.nz/knowledgebase/177/)

3.1 手动添加
推荐通过 导入配置文件(3.2部分)(可以一次性全部导入) / 扫码(3.3部分)  的方式进行添加，本部分主要用于说明节点设置页面各选项的作用。

打开客户端，点击 连接 > 添加 > 手动(M)，在弹出的窗口中按照如下的内容填写。

红框部分为必须填写的内容，绿框部分可以根据情况进行修改，选项说明见图片底部。
![](https://i.loli.net/2020/02/29/qFhAOzfT8u9cQLb.png)
添加节点

+ 配置名称 : 节点的备注名称，可以自由填写
+ 服务器地址： 填写选用的服务器地址域名或是 IP
+ 服务器端口： 我们 Trojan 服务的端口均为 443
+ 密钥： 填写服务连接密码
+ 本地端口 / 本地HTTP端口： SOCKS5 与 HTTP 的监听端口，一般保持默认即可，由于 Trojan / Shadowsocks 客户端默认端口一致，因此不要同时运行两个客户端，如有同时运行需求，请修改其中一个客户端的 Socks5 监听端口
+ 本地服务类型: 选择 SOCKS5 + HTTP 会在连接后提供 HTTP 协议的监听，否则仅监听 SOCKS 端口
+ 自动化： 勾选后会在程序启动时自动连接该节点
点击 OK 后完成添加。

端口设置，请点击顶部菜单 设置 > 高级设置 进行设置，下图为客户端(v0.0.9)的默认设置
![](https://i.loli.net/2020/04/15/eSG2cmCIhJoErVW.png)


3.2 导入配置文件
打开服务详情页面，点击密码底部的 GUI-Config 配置  下载 下载配置文件 gui-config.json。
![](https://i.loli.net/2020/02/24/NWpGqHmiUuPkCI1.png)


然后点击客户端顶部的 文件 > 从 gui-config 导入连接(I) ：

![导入配置文件](https://i.loli.net/2020/02/29/HFcdqJBKQye35iu.png)

导入后选择一个节点再点击顶部的链接按钮进行使用，配置中提供的本地 SOCKS5 端口为 1080 与 Shaodowsocks 客户端默认端口一致，因此点击后如果没有反应请确认没有其他已连接的节点或是其他程序占用了客户端的本地端口。

选中的节点双击可以打开编辑配置，选项说明请查看 3.1 部分。

![](https://i.loli.net/2020/02/29/1QXAn7rs3aR6e29.png)

 

3.3 扫描二维码添加
打开服务详情页面，点击服务器信息最后一列的二维码图标显示二维码。

![显示二维码](https://i.loli.net/2020/02/20/boxhdzwBfM7CgRU.png)

然后点击客户端顶部菜单的 连接 > 添加 > 扫描屏幕上的二维码(S)

![二维码添加](https://i.loli.net/2020/02/20/KTLePmyRSJOuExX.png)

参考手动设置部分的选项说明决定是否修改设置，点击 OK 后完成添加。

![添加节点](https://i.loli.net/2020/02/29/qFhAOzfT8u9cQLb.png)

3.3.1 粘贴 URI 添加

点击客户端顶部菜单的 连接 > 添加 >  URI 

**粘贴 产品详情 -点击 节点地址旁边 齿轮图标 - Trojan Url 下的内容**

### 4. 设置开机启动
点击顶部菜单 设置 > 常规设置 , 勾选 登陆时启动 即可。

![开机启动](https://i.loli.net/2020/02/29/P7YoDJ46rRqy9pN.png)

### 5. 注意事项
Trojan - qt5 与 Shadowsocks-WIN 的客户端默认监听端口均为 1080 ，因此一般情况下请不要同时运行两个客户端。
如果有同时运行需求请修改任意一个客户端的本地端口设置。

### 6. 系统dialing的设置
在 Windows 的通知区域 Trojan 客户端图标上右键打开菜单可以设置系统代理相关内容 

- PAC模式： 设置系统代理，为 PAC 模式，按照 PAC 文件内规则决定访问的网站是否经过代理，推荐日常使用
- 全局模式：设置系统代理，为全局模式，表示电脑中所有使用系统代理的流量都会经过代理
- 直连模式：不设置系统代理，需要手动在软件内设置代理或是安装扩展进行使用

如果菜单不一致，请更新客户端版本

### 7. 浏览器设置
设置方法请参考：[Chrome / Edge / Firefox 安装 Proxy SwitchyOmega 扩展使用](https://portal.shadowsocks.nz/index.php?rp=/knowledgebase/180)