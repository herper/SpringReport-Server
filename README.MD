# SpringReport-Server

## SpringReport服务端

### update list

2025-03-09 update form [springreport/springreport](https://github.com/springreport/springreport)

#### Changelog
>
> ##### 2025-03-09
>
> ##### 分组小计bugbug修复
>
> ##### word报表合并单元格bug修复
>
> ##### 其他已知bug修复
>
> ##### --V2.3.2
>
> ##### 1.填报报表新增主子表填报功能，具体使用可以参考以下文档[[参考文档](https://gitee.com/springreport/springreport/wikis/pages?sort_id=13553757&doc_id=5747656)]
>
> ##### 2.填报报表部分bug修复和操作上的优化
>

#### 感谢蔡老师的开源项目

### 有一些无法下载的依赖包，使用了github的仓库。仓库地址：[herper/mvn-repo][def]

[def]: https://github.com/herper/mvn-repo

### P.S.：pom.xml文件进行了更新，为了方便Github Actions运行，增加了远程源仓库地址

  ```<!-- 配置仓库地址 -->
    <repositories>
        <!-- 官方仓库（优先级最高） -->
        <repository>
            <id>central</id>
            <name>Maven Central</name>
            <url>https://repo.maven.apache.org/maven2</url>
            <releases>
                <enabled>true</enabled>
                <checksumPolicy>fail</checksumPolicy>
            </releases>
            <snapshots>
                <enabled>false</enabled>
            </snapshots>
        </repository>

        <!-- GitHub自定义仓库（备用仓库） -->
        <repository>
            <id>github-mvn-repo</id>
            <name>SpringReport Maven Repo</name>
            <url>https://raw.githubusercontent.com/herper/mvn-repo/main/SpringReport/</url>
            <layout>default</layout>
            <releases>
                <enabled>true</enabled>
                <updatePolicy>daily</updatePolicy>
            </releases>
            <snapshots>
                <enabled>false</enabled>
            </snapshots>
        </repository>
    </repositories>
    ```
