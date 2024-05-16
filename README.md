# 一键生成native层trace脚本
# 1.使用方法
将```stalker_trace_so.py```复制到```[IDA安装目录]\plugins```

在IDA中选择```Edit->Plugins->stalker_trace_so```，将会在so所在的目录下自动生成```trace_xxx.js```

frida运行脚本

```frida -U -l trace_xxx.js -f [package name]```

# 2.小修改
可对带有指定字符的函数名进行hook，可以一键生成对指定函数hook的初步脚本
## 2.1 示例1：对带有crypt的函数trace
![image](https://github.com/FBLeee/IDA_stalker_trace_so_/assets/50468890/4d5f4653-a99f-4f7c-b8c0-a576fe77f806)



## 2.2 示例2：对所有函数trace（空字符）
![image](https://github.com/FBLeee/IDA_stalker_trace_so_/assets/50468890/b9e3c299-810f-4708-bcaf-35f09f23cda5)


# 3.致谢
本IDA插件是基于以下项目修改
**[oacia/stalker_trace_so](https://github.com/oacia/stalker_trace_so)**
