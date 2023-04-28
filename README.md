# 2023-04-27

https://github.com/xuuhaoo/OkSocket

https://www.jianshu.com/p/8ee3ee766265

https://github.com/xuuhaoo/OkSocket/releases

# 

```
allprojects {
    repositories {
        jcenter()
    }
}
```

```
dependencies {
    //基础的 OkSocket 功能集成包.您的Socket开发无论是客户端还是Java,都需要此包 (必须集成)
    api 'com.tonystark.android:socket:4.2.1'
    //如果您需要使用 OkSocketServer 功能在客户端或者Java程序,您还需要依赖下面的Server插件包和上面的一起依赖.
    api 'com.tonystark.android:socket-server:4.2.1'
}
```

```
-dontwarn com.xuhao.didi.socket.client.**
-dontwarn com.xuhao.didi.socket.common.**
-dontwarn com.xuhao.didi.socket.server.**
-dontwarn com.xuhao.didi.core.**

-keep class com.xuhao.didi.socket.client.** { *; }
-keep class com.xuhao.didi.socket.common.** { *; }
-keep class com.xuhao.didi.socket.server.** { *; }
-keep class com.xuhao.didi.core.** { *; }

-keepclassmembers enum * {
    public static **[] values();
    public static ** valueOf(java.lang.String);
}
-keep class com.xuhao.didi.socket.client.sdk.client.OkSocketOptions$* {
    *;
}
-keep class com.xuhao.didi.socket.server.impl.OkServerOptions$* {
    *;
}
```