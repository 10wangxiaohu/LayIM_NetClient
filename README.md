### ��Ŀ���

###### LayIM.NETClient �Ƕ��ڵ�ǰ����ǰ��WebIM���LayIM��˵�ʵ�֡�
###### LayIM��Ŀ��ַ��http://layim.layui.com/
-- ����Ŀ����ѧϰ����ʹ�ã����ʺ������������������ݿ�ΪSQL Server 2008����������ΪVisual Studio 2015.

###### ���ٿ�ʼ
---
 ��һ�����½�MVC��Ŀ����ASP.NET WebForm��Ŀ����� Owin Startup �ࡣ
```
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
���������޸������ļ����������ݿ������ַ��������Ƶ�appkey��appsecret.(�����е�key��secret����ֱ����ȥ������ʹ��)

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
![](http://img1.gurucv.com/image/2017/6/19/0c0b3974be244c41a8f20c14888de28f.png)

--- 
������û�֮��Ĭ�ϵ�һ���û�IDΪ 100000. Ȼ����� http://localhost:6357/?uid=100000 ����չ��LayIMҳ�档
![](http://img1.gurucv.com/image/2017/6/19/2d8f5b5887eb4161aa13b74290b60976.png)

---
ʣ�µ�����Ϳ����Լ����ݽӿ��������ֲ����������磬��Ӻ��ѡ�
![](http://img1.gurucv.com/image/2017/6/19/a9de2a5ea24a4b098c9496f5c4a447ca.png)

---
��Ŀ���ܵ���Ϊֹ��ʣ���������������bug ��С��飬��Ⱥ�˽�ɡ� Ⱥ�ţ�303451512 