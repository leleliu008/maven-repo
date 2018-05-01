# maven-repo
某些SDK只提供了jar、aar等使用起来很不方便，为了便于管理，自己建了一个Maven仓库

## 如何使用
1、在Android工程的根目录下的build.gradle中加入如下配置：
```
allprojects {
    repositories {
        maven {
            url "https://raw.githubusercontent.com/leleliu008/maven-repo/master"
        }
    }
}
```
2、在子模块中的build.gradle的dependencies中添加依赖：
<br><br>
如果您使用的是gradle4.1以下的版本，请使用compile关键字，gralde4.1以上的版本使用api或者implementation这两个关键字其中之一。
<br>
<br>
爱贝：
```
api("com.fpliu:ipay:4.0@aar")
```
Camera360：
```
api("com.fpliu:Camera360:1.9.8@aar")
```
