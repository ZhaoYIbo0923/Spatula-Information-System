# Spatula
The Big Home Work for IS

![](stuprise.gif)





### 与主库同步的方法：

1. 添加主库`https://github.com/TheEightLab/Spatula.git`到你的本地remote：

```shell
$ git remote add eight https://github.com/TheEightLab/Spatula.git
```
上面的句子中，`eight` 是新remote的名字

2. 在本地pull主库的main分支。

```shell
$ git pull eight main
```


### 同步数据库

pull之后记得同步数据库，因为别人可能改表了。

如果需要指定是哪一个模块的表，把下面`[specific_module_name]`换成 Module 的名字。这里用方括号代表是“可选的”。

```shell
$ python manage.py makemigrations [specific_module_name]
$ python manage.py migrate
```

### sqlite spy

开发时先使用sqlite，优点：轻、小、快、无需配置，方便在各开发者处统一。
缺点：无安全性。不支持alter语句。

最大的优点：你可以直接把文件删掉，重新搞一个库出来。

用 sqlite spy， 可以像打开 Excel 表格一样打开 sqlite 文件查看、修改。
https://bhpan.buaa.edu.cn:443/link/181A1B1122055E4B9FCFE9AEE68A684A

### Html模版文件路径问题

请大家在html模版统一存放在这个路径下
```shell
app/templates/app/index.html
```
其中 `app` 为你的应用名称

否则会出现同名模版覆盖的情况

请务必注意此问题！！！
 
# Spatula-Information-System
