 # 如何在Windows7上使用IIS7部署Django Web App
 
 环境：
 1. Windows 7 SP1
 2. IIS 7
 3. Python 3.7
 4. Django 2.2+
 
 原因: 使用Python + Django框架为公司写了一个工具, 需要在内网中部署使用.
 
 主要步骤如下:
 
 1. 打开IIS功能:
 
    - 首先在控制面板中进入"程序", 选择"启用或打开Windows功能", 选上"Internet Information Services", 确定;
 
    - 然后进入"系统和安全", 单击"管理工具", 就可以看到"Internet Information Services(IIS)管理器"了, 双击打开,弹出管理器界面;
 
    - 在左侧"连接"的导航栏可以看到自己的计算机名称, 单击"网站"里的"Default Web Site", 然后单击右侧"操作"界面下的"浏览 \*:80(http)", 后弹出一个网页, 没有错误信息则说明IIS已正常运行.
 
 2. 安装wfastcgi.py模块:
 
 
 3. 设置IIS:
 
 
 
 
 
 
