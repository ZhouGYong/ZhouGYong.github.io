#Cordova��ƽ̨��������

##����
Apache Cordova�ǿ�ƽ̨Ӧ�ÿ���ƽ̨��ʹ��ƽ̨�޹ص�webǰ�˼�����HTML5, javascript��CSS��, ͬʱ�ṩ�˷��ʲ���ϵͳ�ײ��������

Apache Cordova֧������Ӧ������
###�ֿͻ���
ֱ����client sideӦ��HTML5����ҳ�棬Ӧ��javascript������̨�߼����ȿ���һ�����ض������е�App��Ҳ֧��ͨ��ajax����internet web api�ķ��� 
###�ݿͻ���
client side������һ����ʼ���ӣ�Ȼ�����InAppBrowser�����ӣ�Ȼ�����в���������Զ��webҳ�档���ַ�ʽ���Ժܷ���İ�һ�����е�web applicationֱ��wrap��һ��ԭ��App��ֻҪ��ҳ�������ƶ��˵�С��Ļ��

##��װ
  `npm install -g cordova`
  `cordova create MyApp`
  `cd MyApp `
  `cordova platform add android`
  `cordova run android`
��Ҫ�����úö�Ӧƽ̨�ı��벿�𻷾�������android��Ҫ�Ȱ�װandroid studio�ȡ����һ�������ֱ�Ӱѱ���õ�apk����android�ˣ�������ִ�С�

##����
�����洴����MyAppĿ¼�£���Ҫ��עconfig.xml

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
����element content����App����ʱ�ĳ�ʼҳ��, allow-navigation����������App�ڲ�������д򿪵���ҳ���ӣ��Ǵ�·���µ����ӻ���ⲿ�������