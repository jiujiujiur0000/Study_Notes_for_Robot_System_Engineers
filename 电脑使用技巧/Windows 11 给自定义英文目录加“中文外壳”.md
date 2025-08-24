给文件夹添加外壳是Windows 专有特性

1. 在文件夹中新建 `desktop.ini`，内容：  

   ```cmd
   [.ShellClassInfo]
   LocalizedResourceName=<文件夹别名>
   ```

   保存时编码选 **ANSI** 或 **UTF-16 LE（有的记事本里叫 Unicode）**。

2. 给 **文件夹本身** 加系统属性（管理员身份）：  

   ```cmd
   attrib +s "<文件夹路径>"
   ```

3. 给 `desktop.ini` 加系统+隐藏+只读属性（管理员身份）：  

   ```cmd
   attrib +s +h +r "D:\Workspace\desktop.ini"
   ```

4. 刷新资源管理器  
