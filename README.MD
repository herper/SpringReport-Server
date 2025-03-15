# SpringReport-Server

## 开源企业级报表系统SpringReport服务端[感谢蔡老师开源](https://github.com/springreport/springreport)

## 具体使用方法请访问[SpringReport官方网站](https://springreport.vip/)

### update list

#### 2025-03-14 update form [springreport/springreport](https://github.com/springreport/springreport)

#### Release版本已通过Github Actions 打包，下载地址：[Releases](https://github.com/herper/SpringReport-Server/releases/tag/v20250314142301)

##### 2025-03-09 update form [springreport/springreport](https://github.com/springreport/springreport)

#### Changelog
>
> #### 2025-03-14 Springreport V2.3.3
>
> ##### V2.3.3
>
> ##### 1.word版本报表新增onlyoffice支持，功能比canvas-editor更强大
>
> ##### 2.循环块新增分栏支持，分栏效果可以参考下图
>
> ##### 3.excel打印间隔距离bug修复
>
> ##### 4.word纸张类型设置失效bug修复
>
> ##### 5.word导出table合并单元格bug修复
>
> ##### 6.大屏预览自适应优化
>
> ##### 7.其他的已知bug修复
>
> ##### 2025-03-11
>
> ##### Bug Fixes
>
> ##### 2025-03-10
>
> ##### 1.填报报表bug修复
>
> ##### 2.分组小计bug修复
>
> ##### 3.wword(canvas-editor版本)导出表格合并单元格bug修复
>
> ##### 4.大屏预览页面自适应
>
> ##### 5.其他已知bug修复
>
> ##### --V2.3.2
>
> ##### 1.填报报表新增主子表填报功能，具体使用可以参考以下文档[[参考文档](https://gitee.com/springreport/springreport/wikis/pages?sort_id=13553757&doc_id=5747656)]
>
> ##### 2.填报报表部分bug修复和操作上的优化
>
### 有一些无法下载的依赖包，使用了github的仓库。仓库地址：[herper/mvn-repo](https://github.com/herper/mvn-repo)

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
