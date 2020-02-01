 # 如何在Windows 7上使用IIS部署Django Web App
 
 环境：
 1. Windows 7 专业版 SP1
 2. IIS 6.0
 3. Python 3.7
 4. Django 2.2+
 
 原因: 使用Python + Django框架为公司写了一个工具, 需要在内网中部署使用.
 
 主要步骤如下:
 
 1. 打开IIS功能:
 
    1. 首先在控制面板中进入"程序", 选择"启用或打开Windows功能", 选上"Internet Information Services", 确定;
 
    2. 然后进入"系统和安全", 单击"管理工具", 双击打开"Internet Information Services(IIS)管理器", 弹出管理器界面;
 
    3. 在左侧"连接"的导航栏可以看到自己的计算机名称, 单击"网站"里的"Default Web Site", 然后单击右侧"操作"界面下的"浏览 \*:80(http)", 后弹出一个网页, 没有错误信息则说明IIS已正常运行.
 ![Success Site](/images/Success.png)
 
 2. 安装并启用wfastcgi.py模块:
 
    1. 管理员权限下cmd运行pip install wfastcgi
    2. 然后输入wfastcgi-enable命令启用wfastcgi功能, 此时命令行窗口会输出配置成功信息, 其中包含了当前用做 FastCGI script processor 的python路径和wfastcgi路径.
 
 
 3. 设置IIS:
    1. 启用IIS管理器, 右键单击"网站"选项, 选择"添加网站", 如图所示：
    ![Add Site](/images/AddSite.png)
    需填写内容：
      - 网站名称：自己填写
      - 物理路径：Django项目根目录
      - IP地址：电脑IP地址
      - 主机名：跟IP地址一致
      
    2.
   
 
 
 
 
 
