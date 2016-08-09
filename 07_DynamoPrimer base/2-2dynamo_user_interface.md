##Dynamo用户界面

Dynamo的用户界面在5个主要领域组成。其中最大的领域,是视觉编程。

![User Interface Regions](images/2-2/01-UI-Regions.png)

>1. 菜单
2. 工具栏
3. 节点库
4. 工作区
5. 执行区

从这里开始,确认Dynamo的UI,各个领域的详细功能。

####菜单

菜单是唐氏drop Dynamo软件的基本功能的部分可以登陆。很多软件和Windows一样,最初的2个菜单项(上图左边的菜单项目和旁边的菜单项),文件管理的操作、选择和内容进行编辑的操作。其他菜单项在菜单项Dynamo固有的。

![Dropdown Menus](images/2-2/02-Menus.png)
> 1. 文件
2. 编辑
3. 视图
4. 节点发布包
5. 设置
6. 帮助

####工具栏

Dynamo工具栏是[恢复](Ctrl + Z)指令和[](Ctrl + Y)指令的其他文件相关的工作,有助于连接一系列的快递按钮被准备。右边的按钮,使用的スナップショット联盟,可以一下思绪。这个按钮在文档的制作和共享时进行特别方便。

![Needs Update-split location Toolbar](images/2-2/03-Toolbar.png)

> 1. [新]- dyn .制定新的文件时使用。
2. [打开]- dyn .现有的文件(联盟步调)或. dyf文件(定制节点)时使用。
3. [保存]/[名字保存]- dyn .活性的文件和. dyf保存文件时使用。
4. [恢复]-最后的操作时使用回原位。
5. [来]-次的操作,如果重来使用。
6. [形象作为联盟步伐一下思绪]-标示的速度PNG文件,联盟时使用一下思绪。

####节点库
库,附属的既定节点,被追加发展和包装等,定制节点被上载的所有节点都被隔离。库内的节点,其节点数据 **创建** 数据, 执行 **执行**, or **查询** 数据.

##### 参照类
默认情况下,  **Library** 将包含八个类别的节点. **Core** and **Geometry** 是最多包含的节点,因此节点,如果这些寻找最初使用的分类建议。这些范畴为参照,节奏的联盟可以追加的节点阶层、至今没有使用了新的节点最佳的方法寻找简单,可以理解。

> 在这里,既定的节点为中心,后来确认,追加的库,定义节点Package Manager,使用这个库,扩展了。

![NEEDS UPDATE-full width - Library Categories](images/2-2/04-LibraryCategories.png)
>1. Analyze
2. Built-in Functions
3. Core
4. Geometry
5. Migration
6. Office
7. Operators

[存档]菜单点击库,并参照[Geometry] > 点击[Circle]。新的菜单项目(具体来说, **Create** and **Query** 显示,请确认）

![NEEDS UPDATE-use full width - Browsing the Library](images/2-2/05-LibraryBrowsing.png)
>1. 库
2. 类别
3. 子类别:创建/行动/查询
4. 节点
5. 节点描述和属性——这节点图标出现在上空盘旋。

From the same Circle menu, hover your mouse over **ByCenterPointRadius**. The window reveals more detailed information about the Node beyond its name and icon. This offers us a quick way to understand what the Node does, what it will require for inputs, and what it will give as an output.

![Node Pop Up Window](images/2-2/06-NodePopup.png)
>1. Description - plain language description of the Node
2. Icon - larger version of the icon in the Library Menu
3. Input(s) - name,  data type, and data structure
4. Output(s) - data type and structure

#####Searching
If you know with relative specificity which Node you want to add to your Workspace, the **Search** field is your best friend. When you are not editing settings or specifying values in the Workspace, the cursor is always present in this field. If you start typing, the Dynamo Library will reveal a selected best fit match (with breadcrumbs for where it can be found in the Node categories) and a list of alternate matches to the search. When you hit Enter, or click on the item in the truncated browser, the highlighted Node is added to the center of the Workspace.

![Searching the Library](images/2-2/07-LibrarySearching.png)
>1. Search Field
2. Best Fit Result / Selected
3. Alternate Matches

###Settings
From geometric to user settings, these options can be found in the **Settings** menu. Here you can opt in or out for sharing your user data to improve Dynamo as well as define the application's decimal point precision and geometry render quality.

> Note: Remember that Dynamo's units are generic.

![show menu](images/2-2/08-Settings.png)

>1. Enabling Reporting
2. Number Format
3. Render Quality

###Help
If you're stuck, check out the **Help** Menu. Here you can find the sample files that come with your installation as well as access one of the Dynamo reference websites through your internet browser. If you need to, check the version of Dynamo installed and whether it is up to date through the **About** option.

![show menu](images/2-2/09-Help.png)

>1. Samples
2. Report A Bug
3. Go To Project Website
4. Go To Project Wiki
5. Display Start Page
6. About



