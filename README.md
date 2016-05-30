android static check tools
======================

一个由Gradle构建的代码静态检查Demo，具体内容可在[博客](http://98ki.com/how-to-improve-quality-and-syntax-of-your-android-code/)中了解。

工具
-------
代码表态检查应该尽量全面，所以相关的工具就能用都用。
目前集成的工具有 :
 - Checkstyle.
 - Findbugs.
 - PMD.
 - Lint.

运行这些代码检查工具并获取结果报告 :

 ```bash
  gradle check
  ```

Findbugs 是对字节码进行扫描，所以应该构建工程之后再进行扫描 :

 ```bash
   gradle build
 ```

你可以通过修改 [quality.gradle](config/quality.gradle) 这个文件，来定制这个插件。
比如 :
 - 导出的报告类型 (xml 或 html).
 - 如果发生错误是否继续执行.



最后的结果会在 app/build/reports目录下.
