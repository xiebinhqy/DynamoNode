## Revit的关系
![Connection](images/8-1/link.png)

Dynamo,待Revit使用Revit的大厦,型号(BIM)查询功能,数据和逻辑Dynamo的基于视觉算法根据编辑环境可以扩张。Dynamo的灵活性Revit的健全的数据库功能和结合,BIM的新的可能性。

在这一章里,使用了Dynamo BIM流程说明。该章的各章节中,演习,并确认BIM。BIM的视觉算法编辑功能的机制的理解是,样品的项目中实际操作的最佳方法。不过在这之前,Dynamo的历史,简单的解释。

####Dynamo的历史
![History](images/8-1/earlyScreenshot.png)
> Dynamo项目,开发小组和社区的积极支持而发展到这里了,最初的目标是小了。

Dynamo,本来Revit的设计流程合理化被开发了。Revit在每一个数据库项目的制作,用户界面的制约,不接受这个信息,一般用户来说很难。 Revit是概括性的API(应用程序接口),因此被第三方开发人员使用这些API,基因学的工具可以制作。如果程序员已经习惯这个API,用户编程的经验来说,文本为基础的脚本,叙述的是简单的事。Dynamo的开发团队,易懂的视觉算法编辑器提供的数据,Revit可以轻易操作的目标。

Revit的基因学和Dynamo的主要节点组合起来使用,相互运用性,设计制作、图书等方面解析,生成模型,参数控制的作业流程的范围大大拓展。如果使用Dynamo,麻烦的作业流程作业的自动化,设计工作可以集中。


###在Revit运行Dynamo
![Connection](images/8-1/01.png)
>1. Revit编辑器,链接到外接程序,然后单击“Dynamo”。注意:Dynamo将只能打开运行的文件。
> 1. Revit项目的家庭编辑器中,[插件]tab开始[* Dynamo *点击。在Dynamo Dynamo起动的文件内,只实行请注意。


![Connection](images/8-1/00.png)
>1. 在Revit中打开Dynamo时,有一个新的类别叫* *“Revit” 。这是一个综合的UI提供专门Revit工作节点。*
> 1. 在起动Revit Dynamo,Dynamo的库内[* Revit *]的新范畴。这个新的类别,Revit流程专用的节点可以访问。


**注 - Dynamo Revit固有的家庭用图表处理节点的情况下,使用图表是在正在运行Revit Dynamo打开时只正常动作。例如,在正在运行Revit Dynamo的图表,Dynamo Sandbox举行Revit节点被丢失.*


### 冻结的节点


Revit在健全的项目管理提供平台,因此Dynamo的参数根据情况操作变得复杂,计算速度下降。If Dynamo is taking a long time to calculate nodes, Dynamo的节点计算需要时间,则节点“死机”的功能,使用图表的开发中相关操作运行Revit可以停止。节点的死机问题,操作的详细[solids chapter](../05_Geometry-for-Computational-Design/5-6_solids.md#freezing)请参照。

### 社区
Dynamo,原本建筑设计人员和结构设计人员开发的工具。Dynamo的社区,是建设行业的专家和交流并可以学习场所,目前也在持续增长。Dynamo的社区的信息共享和开发项目,积极参加建筑设计,结构设计人员,根据程序员,设计师组成。

Dynamo在持续进化到开源项目中去,其开发的大部分是Revit有关。专题论坛,提问[posting questions](http://dynamobim.org/forums/forum/dyn/)投稿请。作为程序员如果参与Dynamo项目,是下面的链接,请参照:[github page.](https://github.com/DynamoDS/Dynamo)GitHub的Dynamo页。另外,[Dynamo Package Manager](http://dynamopackages.com/)那么,各种第三方产库提供。被提供的包装,大多是建设行业的作业流程中使用的目的是制定。实际上,面板制作用的第三方制造包装使用一下吧。

![Blog](images/8-1/blog.png)
> Dynamo开发团队,[Blog](http://dynamobim.com/blog/)频繁更新。最近的报道,最新的开发确认请获取信息。


