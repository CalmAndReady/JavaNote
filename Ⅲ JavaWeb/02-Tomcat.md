# 一、Tomcat安装与配置
## 1）Tomcat服务器官网地址:
 https://tomcat.apache.org/
## 2）Tomcat服务器下载地址：
 https://tomcat.apache.org/download-90.cgi
## 3）Tomcat服务器安装
凡是Apache组织提供的工具，都是绿色免安装版。只要将压缩包进行解压缩即可
## 4）Tomcat服务器配置:
### 1.JAVA_HOME 环境变量:
- 介绍： windows提供一个环境变量。JAVA_HOME存储当前计算机中JDK安装地址。
- 作用:  为今后所有在当前计算机上安装的由Java开发工具来提供当前计算机中JDK位置
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706143324.png)
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706143625.png)
### 2.CATALINA_HOME 环境变量:
- 介绍：windows提供的一个环境变量。CATALINA_HOME存储Tomcat服务器在当前计算机中存储位置。
- 作用：Tomcat服务器安装在windows操作系统，启动与关闭需要由windws系统负责
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706143435.png)
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706143600.png)
# 二、Tomcat服务器启动与关闭
## 1）Tomcat服务器的管理命令位置
Tomcat服务器安装位置/bin 
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706143832.png)

## 2）启动Tomcat
1. 进入到bin文件夹下
2. 在bin文件夹下进入到DOS窗口中
3. 在DOS窗口的命令行下，输入 startup  来通知windows系统启动Tomcat服务器
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706144011.png)
## 3）关闭Tomcat
1. 关闭【Tomcat窗口】 ，让Tomcat服务器处于休眠状态
2. 在DOS窗口中， 输入 shutdown，真正的关闭Tomcat服务器

![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706144043.png)
# 三、第一次BS通信：
1. 创建一个网站：
- 网站存储位置：在windows启动Tomcat之后，要求Tomcat在接收到请求之后，只能到Tomcat安装位置/webapps文件夹下寻找【网站】
- 网站：一个网站仅仅就是一个文件夹而已。网站名称不能是中文
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706144432.png)
2. 创建一个静态资源文件在网站下创建one.txt，网站中资源文件名称不能是中文
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706144613.png)
3. 启动tomcat，可以随时接收浏览器发送的请求
4. 打开浏览器，向Tomcat服务器发送请求，索要资源文件
	- 请求地址格式:  http:// 服务端计算机IP地址:Http服务器端口号/网站名/资源文件.后缀名
	- Tomcat服务器的端口号:8080
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706144949.png)
# 四、IDEA管理Tomcat
## 1）设置
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706145406.png)
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706145427.png)

## 2）IDEA创建网站
### 1.创建
通过以下步骤创建两个网站（01-第一个网站 & 02-第二个网站）
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706145649.png)
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706145729.png)

### 2.网站结构
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706151354.png)
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706151412.png)

### 3.发布
将发布第一个网站
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706150126.png)
添加第一个网站
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706150228.png)
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706150304.png)
设置同步更新![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706151536.png)
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706150559.png)
👍成功！
![](../00-resource/assets/JavaWeb/Pasted%20image%2020220706151008.png)