# gradle-publish

1.build.gradle 中 添加代码

buildscript {
    repositories {
        jcenter()
    }
    dependencies {
        classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.6'
        classpath 'com.github.dcendents:android-maven-gradle-plugin:1.3'
    }
}

allprojects {
    repositories {
        jcenter()
    }
}


2.build.gradle最后添加
apply from: 'https://raw.githubusercontent.com/imflyn/gradle-publish/master/bintray.gradle'

3.gradle.properties 中定义变量

bintray_user=
bintray_api_key=

bintray_group=

bintray_version=

bintray_name=

bintray_repo=

bintray_siteUrl=

bintray_gitUrl=

bintray_issuesUrl=

bintray_desc=

bintray_labels =   //['aar', 'android', 'test']

4.rebuild 后执行 gradle bintrayUpload 命令
