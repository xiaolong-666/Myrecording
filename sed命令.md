# sed命令

## 替换匹配内容的下一行
```bash
sed -i '/ATTest/{n;n;s/"actual.*/"actual": "123.123.123"/;}' amd64_ut_data.json
```
其中 `n`代表下一行

替换模式：

![](https://pic4.zhimg.com/80/v2-31f5d953a3cd62eaf71d317fb58dbed3_720w.jpg)



**`&`**号，再重复一遍。当它用在替换字符串中的时候，代表的是原始的查找匹配数据。

> **[&]** 表明将查找到的数据使用[]包围起来。
> **“&”** 表明将查找的数据使用””包围起来。

下面这条命令，将会把文件中的每一行，使用引号包围起来。

```bash
sed 's/.*/"&"/' file
```



链接：https://zhuanlan.zhihu.com/p/66651350
