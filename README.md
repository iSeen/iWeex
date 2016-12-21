# iWeex
alibaba / weex:  
[GitHub](https://github.com/alibaba/weex)  
[官网](http://alibaba.github.io/weex)

Weex是阿里开源的一套构建跨平台的移动框架。  
对于前端的同学，最直观的是web components的开发方式；  
对于Native同学，可以理解为使用web的开发方式构建跨平台移动程序（iOS & Android）。  
可以类比的是React Native，但是相对React Native更为彻底：不仅统一了 iOS/Android的差异，更是实现了三端的统一。


### 配置环境
##### 1.安装Node.js
	$ node -v
	v6.3.1
	$ npm -v
	3.10.3
node -v 和 npm -v 命令来测试Node.js环境是否搭建成功;

##### 2.安装weex-toolkit

	npm install -g weex-toolkit   使用npm安装
	
	如果很慢，考虑使用cnpm来安装 (cnpm是一个国内npm镜像，可以提高下载速度)
	npm install -g cnpm     全局安装cnpm
	
	cnpm install -g weex-toolkit   使用cnpm安装, 若提示权限问题，可加上sudo关键字即可:
	sudo npm install -g weex-toolkit   输入本机电脑密码即可.
	
	weex --version   检查是否安装成功
	info 0.6.4 


### 初始化项目
1.`pod init` 新建Podfile, 
`open Podfile` 打开,输入  

	target 'iWeex' do
	pod 'WeexSDK', :path=>'./sdk/'
	end

2.下载[官方Weex项目](https://github.com/alibaba/weex.git)  
在ios目录下有个sdk文件夹，把它复制到初始化项目的根目录，和Podfile文件路径一致;

3.关掉xcode，在当前根目录，命令行执行 `pod install`，完成后以后使用xcworkspace文件打开项目;

4.创建一个新目录weex，命令行cd到weex目录，执行weex init，会提示你输入项目名称;

5.在当前weex目录执行npm install，安装依赖库;

6.weex目录下创建一个文件夹js，weex目录下执行 `weex src -o js` 生成最终需要的js文件;

7.加载weex页面:
xcode打开workspace项目文件, 添加内容详见AppDelegate.m. 

8.将之前创建的js文件夹拖到xcode工程的文件列表;  
弹框选择注意:  不选copy, 选择第二项蓝色文件夹, 选择target.

9.ViewController添加相关代码;

### 参考链接:  
[Weex社区](http://www.jianshu.com/collection/f152a6d31479)

[Weex中文文档](http://www.weex.help/topic/57792770eb60516a48db5485)

[vue.js](http://cn.vuejs.org): 渐进式 JavaScript 框架

[初识与安装](https://vczero.github.io/weex-learning/001_helloworld.html)

