### ��Ŀ���

###### LayIM.NETClient �Ƕ��ڵ�ǰ����ǰ��WebIM���LayIM��˵�ʵ�֡�
###### LayIM��Ŀ��ַ��http://layim.layui.com/
-- ����Ŀ����ѧϰ����ʹ�ã����ʺ������������������ݿ�ΪSQL Server 2008����������ΪVisual Studio 2015.

###### ���ٿ�ʼ
---
 ��һ�����½�MVC��Ŀ����ASP.NET WebForm��Ŀ����� Owin Startup �ࡣ
```c#
 public class Startup
     {
        public void Configuration(IAppBuilder app)
        {
            //ʹ��SQL Server
            GlobalConfiguration.Configuration.UseSqlServer("LayIM_Connection");

            //ʹ��layim api 
            app.UseLayimApi();
        }
     }
```

---
�ڶ������������ݿ�ű�����ǰδ�Զ�������Ҫ�ֶ����У� LayIM.SqlServer/layim.sql

---
���������޸������ļ����������ݿ������ַ��������Ƶ�appkey��appsecret.(�����е�key��secret����ֱ����ȥ������ʹ��,`Ϊ��ֹ�û���Ϣ���������˺Ŷ����������Լ���������key��secret`)

```
	<!--��������-->
    <add key="RongCloud_AppKey" value="pvxdm17jpv1or"/>
    <add key="RongCloud_AppSecret" value="Co2RwQhzkL6G8i"/>
```

```
    <connectionStrings>
		<add name="LayIM_Connection" connectionString="server=192.168.1.18;user id=sa;password=123123;database=LayIM;Min Pool Size=16;Connect Timeout=500;"/>
    </connectionStrings>
```

--- 
���Ĳ��������ص�layui�ļ��з�����Ŀ�� Scripts �ļ����¡����ο�MVCSamples��Ŀ��

--- 
���岽��������Ŀ�����гɹ���������Ŀ���������ݡ����Է��� http://localhost:6357/api �е�����û��ӿ����Ӳ����û���

--- 
������û�֮��Ĭ�ϵ�һ���û�IDΪ 100000. Ȼ����� http://localhost:6357/?uid=100000 ����չ��LayIMҳ�档

---
��Ŀ���ܵ���Ϊֹ��ʣ���������������bug ��С��飬��Ⱥ�˽�ɡ� Ⱥ�ţ�303451512 

--- 
����Ϊ���Խ�ͼ��

![](http://img1.gurucv.com/image/2017/6/19/f045156db6744b5eb0c7e2598308c2e1.png)
![](http://img1.gurucv.com/image/2017/6/19/b64e793eec3a48fa9f060213970477c7.png)
![](http://img1.gurucv.com/image/2017/6/19/4dd5e0f5a658479fb3895c206c4796fe.png)
![](http://img1.gurucv.com/image/2017/6/19/deee85dd76c2444abe266110811a0b57.png)