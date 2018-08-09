#Cordova跨平台开发入门

##介绍
Apache Cordova是跨平台应用开发平台，使用平台无关的web前端技术如HTML5, javascript和CSS等, 同时提供了访问操作系统底层的桥梁。

Apache Cordova支持两种应用类型
###胖客户端
直接在client side应用HTML5构造页面，应用javascript开发后台逻辑，既可是一个本地独立运行的App，也支持通过ajax访问internet web api的服务。 
###瘦客户端
client side仅配置一个初始链接，然后调用InAppBrowser打开连接，然后所有操作都基于远程web页面。这种方式可以很方便的把一个现有的web application直接wrap成一个原生App，只要网页可适配移动端的小屏幕。

##安装
  `npm install -g cordova`
  `cordova create MyApp`
  `cd MyApp `
  `cordova platform add android`
  `cordova run android`
需要先配置好对应平台的编译部署环境，例如android需要先安装android studio等。最后一行命令会直接把编译好的apk部署到android端，并启动执行。

##配置
在上面创建的MyApp目录下，主要关注config.xml

```<?xml version='1.0' encoding='utf-8'?>
<widget id="io.cordova.hellocordova" version="1.0.0" xmlns="http://www.w3.org/ns/widgets" xmlns:cdv="http://cordova.apache.org/ns/1.0">
    <name>hellocordova</name>
    <description>
        A sample Apache Cordova application that responds to the deviceready event.
    </description>
    <author email="dev@cordova.apache.org" href="http://cordova.io">
        Apache Cordova Team
    </author>
    <content src="http://example.com/login.html" /> 
    <plugin name="cordova-plugin-whitelist" spec="1" />
    <access origin="*" />
    <allow-intent href="http://*/*" />
    <allow-intent href="https://*/*" />
    <allow-intent href="tel:*" />
    <allow-intent href="sms:*" />
    <allow-intent href="mailto:*" />
    <allow-intent href="geo:*" />
    <allow-navigation href="http://example.com/*" /> 
    <platform name="android">
        <allow-intent href="market:*" />
    </platform>
    <platform name="ios">
        <allow-intent href="itms:*" />
        <allow-intent href="itms-apps:*" />
    </platform>
    <plugin name="cordova-plugin-navigationbar" spec="^1.0.31" />
    <engine name="browser" spec="^5.0.3" />
    <engine name="ios" spec="^4.5.5" />
    <engine name="android" spec="^7.0.0" />
</widget>
```
其中element content配置App启动时的初始页面, allow-navigation配置允许在App内部浏览器中打开的网页连接，非此路径下的连接会打开外部浏览器。