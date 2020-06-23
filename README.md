# file-leak-detector
Java agent that detects file handle leak
查看java进程文件句柄泄露

`$java -javaagent:./file-leak-detector-1.8-jar-with-dependencies.jar=http=19999 -jar xxx.jar` \
`$java -jar file-leak-detector-1.8-jar-with-dependencies.jar pid http=19999` \
简单总结，JVM 暴露了一些动态操作已加载类型的接口，javaagnet 就是利用这些接口的一个实现，通过 agent 类的固定方法可以执行一些操作，比如对已经加载的类注入字节码，最常用的是用来监控运行时，进行一些疑难 bug 追踪。
