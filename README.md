# 原README:[https://github.com/alibaba/DataX](https://github.com/alibaba/DataX)
# 编译所需步骤
1. 缺少依赖：**org.pentaho.pentaho-aggdesigner-algorithm:jar:5.1.5-jhyde**，从[https://public.nexus.pentaho.org/#browse/search=keyword%3Dpentaho-aggdesigner-algorithm:dfbef09efe1644eaf46667ad068c6bc7:0ab80a743921e426879e5d032aabde8f](https://public.nexus.pentaho.org/#browse/search=keyword%3Dpentaho-aggdesigner-algorithm:dfbef09efe1644eaf46667ad068c6bc7:0ab80a743921e426879e5d032aabde8f)下载jar包，使用命令安装jar包到本地maven库：
```
mvn install:install-file -DgroupId=org.pentaho -DartifactId=pentaho-aggdesigner-algorithm -Dversion=5.1.5-jhyde -Dpackaging=jar -Dfile={your path}/pentaho-aggdesigner-algorithm-5.1.5-jhyde-jhyde.jar
```

2、缺少依赖：**eigenbase:eigenbase-properties:jar:1.1.4**，从[https://github.com/julianhyde/eigenbase-properties](https://github.com/julianhyde/eigenbase-properties)下载源码到本地，该项目版本最新不是1.1.4了，需要修改
pom中的版本号为1.1.4并增加对应的groupId，然后去掉其<parent>标签：
```
  <groupId>eigenbase</groupId>
  <artifactId>eigenbase-properties</artifactId>
  <version>1.1.4</version>
  <packaging>jar</packaging>
```
然后进入pom根目录`mvn install`即可
