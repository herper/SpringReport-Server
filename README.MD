# SpringReport-Server

## 开源企业级报表系统SpringReport服务端

感谢蔡老师开源：[springreport/springreport](https://github.com/springreport/springreport)

## 具体使用方法

请访问 [SpringReport官方网站](https://springreport.vip/)

## 更新日志

### 2026年1月1日
#### 报表功能增强
- 查询条件配置：报表查询条件位置新增配置项，可灵活配置显示在表头或侧边栏弹出
- 模板管理：新增模板导出与导入功能，方便进行数据的迁移与复用
- 自定义函数扩展：
  - 新增 `srf.systemValue` 函数，用于在 Excel 报表中获取系统变量
  - 新增 `srf.paramValue` 函数，用于在 Excel 报表中获取页面参数
  - 新增 `srf.index` 和 `srf.concat` 函数，丰富计算与字符串处理能力
  - 新增自定义函数插件，支持更灵活的函数扩展与管理

#### 打印优化
- 新增打印缩放设置，提升打印布局灵活性
- 优化 Excel 打印性能
- 修复 Excel 打印时，合并单元格超过一页导致的 `Infinite table loop` 异常

#### 条件格式与计算优化
- 修复 LuckySheet 条件格式相关 bug
- 修复 LuckySheet 右下角计算精度问题及过滤隐藏行参与计算的 bug

#### WORD 报表增强
- 表格新增单元格分组合并功能

#### 大屏功能升级
- 组件新增：
  - 选项卡组件，支持多视图切换
  - 地图表格组件，结合地理信息展示数据
  - 卡片列表组件，丰富数据展示形式
  - 数字翻牌器组件，增强动态数据表现力
- 功能增强：
  - 大屏组件新增下钻功能，支持层级数据探索
  - 大屏表格组件新增进度条设置，优化数据可视化效果
  - 大屏设计 UI 更新，提升操作体验

#### 数据与计算优化
- 数据源扩展：新增对 MongoDB 的支持
- 数据字典优化：新增 SQL 语句和自定义方式配置，提高灵活性
- 计算功能增强：
  - 小计单元格新增数值单位转换功能
  - 汇总计算新增同比、环比计算支持
  - 循环块新增子循环块配置，支持更复杂的数据处理逻辑

#### 系统与体验优化
- 演示与文档：官网 Demo 全面更新，并新增功能录制视频讲解，帮助用户快速上手

---

### 2025-03-14 Springreport V2.3.3
- Word 版本报表新增 OnlyOffice 支持，功能比 Canvas-Editor 更强大
- 循环块新增分栏支持
- Excel 打印间隔距离 bug 修复
- Word 纸张类型设置失效 bug 修复
- Word 导出 table 合并单元格 bug 修复
- 大屏预览自适应优化
- 其他已知 bug 修复

---

### 2025-03-11
- Bug Fixes（具体修复内容未详细说明）

---

### 2025-03-10
- 填报报表 bug 修复
- 分组小计 bug 修复
- Word（Canvas-Editor 版本）导出表格合并单元格 bug 修复
- 大屏预览页面自适应
- 其他已知 bug 修复

---

### V2.3.2
- 填报报表新增主子表填报功能，具体使用可以参考以下文档：[[参考文档](https://gitee.com/springreport/springreport/wikis/pages?sort_id=13553757&doc_id=5747656)]
- 填报报表部分 bug 修复和操作上的优化

## 依赖说明

有一些无法下载的依赖包，使用了 GitHub 的仓库。仓库地址：[herper/mvn-repo](https://github.com/herper/mvn-repo)

## 注意事项

pom.xml 文件进行了更新，为了方便 GitHub Actions 运行，增加了远程源仓库地址：

```xml
<!-- 配置仓库地址 -->
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

    <!-- GitHub 自定义仓库（备用仓库） -->
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

## 下载地址

Release 版本已通过 GitHub Actions 打包，下载地址：[Releases](https://github.com/herper/SpringReport-Server/releases/tag/v20250314142301)