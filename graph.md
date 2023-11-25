## 图形介绍

### 流程图(Flowchart)

- 流程图由节点(Unicode几何图形列表)和边(箭头或线)组成。`mermaid`定义了节点和边是如何生成的，并且包含了不同的箭头类型、多方向箭头以及任何与子图的链接。

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

### 时序图 (Sequence diagram)

- 时序图是一个交互图，它显示了各个进程之间是如何运作的，以及它们是以什么顺序运作的。

```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John:Hello John,how are you
    loop Health Cheack
        John->>John:Fight against hypochondria
    end
    Note right of John:Rational thoughts <br/>prevail
    John->>Alice:Great!
    John->>Bob:How about you?
    Bob->>John:Jolly good
```

### 甘特图(Gantt diagram)

- 甘特图是柱状图的一种，首先由卡罗尔 · 阿达米耶茨基(Karol Adamiecki)在1896年开发，然后在1910年代由亨利 · 甘特(Henry Gantt)独立开发，它说明了一个项目的进度表以及任何一个项目完成所需的时间。甘特图说明了终端元素和项目摘要元素的开始日期和完成日期之间的天数。

```mermaid
gantt
dateFormat YYYY-MM-DD
title Adding GANTI diagram to mermaid
excludes weekdays 2014-01-10

section A section
Completed task      :done, des1,2014-01-06,2014-01-08
Active task     :active, des2,2014-01-09,3d
Future task     :   des3,after des2,5d
Future task2     :   des4,after des3,5d
```

### 类别图(Class diagram)

- 在软件工程中，统一建模语言中的类图(UML)是一种静态结构图，通过显示系统的类、属性、操作(或方法)以及对象之间的关系来描述系统的结构。

```mermaid
classDiagram
class01 <|--AveryLongClass :cool
class03 *--Class04
class05 o-- class06
class07 .. class08
class09--|> C2
class09 --* C3
class09 --|> class07
class07:equal()
class07:object[] elementData
class01:size()
class01:int chimp
class01: int gorilla
class08<-->C2:coollabel
```

### Git graph

- Git Graph 是 Git 提交和 Git 操作(命令)在不同分支上的图形化表示。

```mermaid
gitGraph
    commit
    commit
    branch develop
    commit
    commit
    commit
    checkout main
    commit
    commit
```

### 实体关系图(Entity Relationship Diagram)

- 实体关系模型(ER 模型)描述了特定知识领域中相互关联的事物。基本 ER 模型由实体类型(对感兴趣的事物进行分类)组成，并指定实体之间可以存在的关系(这些实体类型的实例)

```mermaid
erDiagram
    course ||--o{ order:places
    order ||--|{ LINE-ITEM:cotains
    course}|..|{ delivery-address:uses
```



### 用户行程图(User Journey Diagram)

- 用户旅行详细地描述了不同用户在系统、应用程序或网站中完成特定任务所采取的具体步骤。这种技术显示了当前(原样)的用户工作流，并揭示了未来工作流的改进领域。

```mermaid
journey
    title My working day
    section Go to work
        Make tea: 5:Me
        Go upstair:3:Me
        Do work:1:Me,cat
    section Go home
        Go diownstair:5:Me
        Sit down:5:Me
```
### 象限图(Quadrant Chart)

- 象限图是分为四个象限的数据的可视化表示。它用于在二维网格上绘制数据点，其中一个变量表示在 x 轴上，另一个变量表示在 y 轴上。象限是通过将图表根据一组特定于所分析数据的标准划分为四个相等的部分来确定的。象限图经常用于识别数据的模式和趋势，并根据图表中数据点的位置确定行动的优先次序。它们通常用于商业、营销和风险管理等领域。

```mermaid
quadrantChart
    title Reach and enagement of campaigns
    x-axis Low Reach--> High Reach
    y-axis Low Eangement--> High Enagement
    quadrant-1 We should expand
    quadrant-2 Need to promote
    quadrant-3 Re-evaluate
    quadrant-4 May be improved
    Campaign A:[0.3,0.6]
    Campaign B:[0.45,0.23]
    Campaign C:[0.6,0.9]
```


### 状态图(State diagrams)

- 状态图是计算机科学和相关领域中用来描述系统行为的一种图。状态图要求所描述的系统是由有限数量的状态组成的; 有时，情况确实如此，而在其他时候，这是一个合理的抽象。

```mermaid
---
title:Simple sample
---
stateDiagram-v2
    [*]-->still
    still-->[*]

    still-->moving
    moving-->still
    moving-->crash
    crash-->[*]
```

### 饼图(Pie Chart Diagram)

- 饼图(或圆形图)是一种圆形的统计图形，它被分成若干片来说明数字的比例。在饼图中，每个切片的弧长(因此其中心角度和面积)与它所代表的数量成正比。虽然它的命名是因为它类似于已经切片的馅饼，但是它的呈现方式也有变化。已知最早的饼状图通常要归功于威廉·普莱费尔1801年的《统计简报》


```mermaid
pie title Pets adopted by volunteers
    "Dogs":386
    "Cats":85
    "Rats":15
```

### 需求图(Requirement Diagram)

- 需求图为需求及其相互之间的连接以及其他文档化的元素提供了可视化。建模规范遵循由 SysML v1.6定义的规范。


```mermaid
requirementDiagram

    requirement test_req{
        id:1
        text:the text 
        risk:high
        verifymethod:test
    }

    element test_entity{
        type:simulation
    }

    test_entity - satisfies -> test_req
```

### 思维导图

- 思维导图: 这是目前的一个实验图。语法和属性可以在以后的版本中更改。语法是稳定的，除了图标集成是实验部分。
```mermaid
mindmap
    root((mindmap))
        Origins
            long history
            ::icon(fa fa-book)
            Popularisation
                british popular psychology author Tony Buzan
        Research
            On effectiveness<br/>and features
            On Automatic creation
                Uses
                    Creative techniques
                    Strategic planning
                    Argument mapping
        Tools
            Pen and paper
            Mermaid
```

### 时间线(Time Diagram)

- 时间轴: 这是目前的实验图。语法和属性可以在以后的版本中更改

```mermaid
timeline 
    title History of Social Media Platform
    2002 : Linkedin
    2004 : Facebook
         : Google
    2005 : Youtube
    2006 : Twitter
```

### 时序图(ZenUML)

- 时序图是一个交互图，它显示了各个进程之间是如何运作的，以及它们是以什么顺序运作的,这个时序图相比于Sequence Diagram来说功能更多

```mermaid
zenuml
    title demo
    Alice->John:Hello John,how are you
    John->Alice:Great!
    Alice->John:see you later
```

### Sankey Diagram
- Sankey 图是用于描述从一组值到另一组值的流程的可视化图。


```mermaid
---
config:
  sankey:
    showValues: false
---
sankey-beta

Agricultural 'waste',Bio-conversion,124.729
Bio-conversion,Liquid,0.597
Bio-conversion,Losses,26.862
Bio-conversion,Solid,280.322
Bio-conversion,Gas,81.144
Biofuel imports,Liquid,35
Biomass imports,Solid,35
Coal imports,Coal,11.606
Coal reserves,Coal,63.965
Coal,Solid,75.571
District heating,Industry,10.639
District heating,Heating and cooling - commercial,22.505
District heating,Heating and cooling - homes,46.184
Electricity grid,Over generation / exports,104.453
Electricity grid,Heating and cooling - homes,113.726
Electricity grid,H2 conversion,27.14
Electricity grid,Industry,342.165
Electricity grid,Road transport,37.797
Electricity grid,Agriculture,4.412
Electricity grid,Heating and cooling - commercial,40.858
Electricity grid,Losses,56.691
Electricity grid,Rail transport,7.863
Electricity grid,Lighting & appliances - commercial,90.008
Electricity grid,Lighting & appliances - homes,93.494
Gas imports,Ngas,40.719
Gas reserves,Ngas,82.233
Gas,Heating and cooling - commercial,0.129
Gas,Losses,1.401
Gas,Thermal generation,151.891
Gas,Agriculture,2.096
Gas,Industry,48.58
Geothermal,Electricity grid,7.013
H2 conversion,H2,20.897
H2 conversion,Losses,6.242
H2,Road transport,20.897
Hydro,Electricity grid,6.995
Liquid,Industry,121.066
Liquid,International shipping,128.69
Liquid,Road transport,135.835
Liquid,Domestic aviation,14.458
Liquid,International aviation,206.267
Liquid,Agriculture,3.64
Liquid,National navigation,33.218
Liquid,Rail transport,4.413
Marine algae,Bio-conversion,4.375
Ngas,Gas,122.952
Nuclear,Thermal generation,839.978
Oil imports,Oil,504.287
Oil reserves,Oil,107.703
Oil,Liquid,611.99
Other waste,Solid,56.587
Other waste,Bio-conversion,77.81
Pumped heat,Heating and cooling - homes,193.026
Pumped heat,Heating and cooling - commercial,70.672
Solar PV,Electricity grid,59.901
Solar Thermal,Heating and cooling - homes,19.263
Solar,Solar Thermal,19.263
Solar,Solar PV,59.901
Solid,Agriculture,0.882
Solid,Thermal generation,400.12
Solid,Industry,46.477
Thermal generation,Electricity grid,525.531
Thermal generation,Losses,787.129
Thermal generation,District heating,79.329
Tidal,Electricity grid,9.452
UK land based bioenergy,Bio-conversion,182.01
Wave,Electricity grid,19.013
Wind,Electricity grid,289.366
```

## 教学

### 流程图(Flowchart)

#### 显示方向
```mermaid
graph TB;
A[这是一个实例]
B[我是来凑数的]
A-->B
```
---
```mermaid
graph BT;
A[这是一个实例]
B[我是来凑数的]
A-->B
```
---

```mermaid
graph LR;
A[这是一个实例]
B[我是来凑数的]
A-->B
```
---
```mermaid
graph RL;
A[这是一个实例]
B[我是来凑数的]
A-->B
```
#### 节点形状

```mermaid
---
title: 节点形状
---
graph TB;
box1(A node with round edges)
box2([A stadium-shaped node])
box3[[A node in a subroutine shape]]
box4[(A node in a cylindrical shape)]
box5((A node in the form of a circle))
box6>A node in an asymmetric shape]
box7{A node rhombus}
box8{{A hexagon node}}
box9[/Parallelogram/]
box10[\Parallelogram alt\]
box11[/Trapezoid\]
box12[\Trapezoid alt/]
box13(((Double circle)))
box1-->box2-->box3-->box4-->box5-->box6-->box7
box8-->box9-->box10-->box11-->box12-->box13
```
#### 箭头形状

```mermaid
---
title: 箭头形状
---
graph LR;
A-->B
C---D
E--TEXT---F
E--TEXT-->F
G-.->H
G-.TEXT.->H
I==>J
I==TEXT==>J
K~~~L
a-->b & c-->d
M o--o N
N <--> O
O x--x P
```
#### 子图

```mermaid
graph TB;
C1-->B1
    subgraph one
    A1---B1
    end
    subgraph two
    C1-->C2
    end
```

```mermaid
graph TB;
    subgraph TOP
        subgraph A1
        direction LR
        F1-->F2
        end
        subgraph A2
        direction TB
        B1-->B2
        end
    end
```
```mermaid
graph TB;
  Start(开始)-->Open[打开冰箱门]
  Open --> Put[把大象放进去]
  Put --> IsFit{"冰箱小不小？"}

  IsFit --> |不小|Close[把冰箱门关上]
  Close --> End(结束)

  IsFit --> |小|Change[换个大冰箱]
  Change --> Open
```

```mermaid
---
title: 前端学习路线
---
graph TB;
A[前端]-->html
A-->css
A-->JS
A-->Node.js
A-->Webpack
A-->VUe
VUe-->F
VUe-->B
```
### Journey
```mermaid
journey
    title My weekday
    section Go school
        经济学: 5:Me
        睡觉: 5:Me,Deng
        Access: 3:Me,Deng,X,W
    section Back home
        play cf: 5:Me
        have dinner: 4:Me,Deng
        running:1:Me
```
### Gantt


```mermaid
gantt
    title A Gantt Diagram
    dateFormat YYYY-MM-DD
    section Section
        A task          :a1, 2014-01-01, 30d
        Another task    :after a1, 20d
    section Another
        Task in Another :2014-01-12, 12d
        another task    :24d
```

```mermaid
gantt
    apple :a, 2017-07-20, 1w
    banana :crit, b, 2017-07-23, 1d
    cherry :active, c, after b a, 1d
```

```mermaid
gantt
    dateFormat HH:mm
    axisFormat %H:%M
    Initial milestone : milestone, m1, 17:49, 2m
    Task A : 10m
    Task B : 5m
    Task C :crit,2m
    Final milestone : milestone, m2, 18:08, 4m
```

```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       Adding GANTT diagram functionality to mermaid
    excludes    weekends
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    section A section
    Completed task            :done,    des1, 2014-01-06,2014-01-08
    Active task               :active,  des2, 2014-01-09, 3d
    Future task               :         des3, after des2, 5d
    Future task2              :         des4, after des3, 5d

    section Critical tasks
    Completed task in the critical line :crit, done, 2014-01-06,24h
    Implement parser and jison          :crit, done, after des1, 2d
    Create tests for parser             :crit, active, 3d
    Future task in critical line        :crit, 5d
    Create tests for renderer           :2d
    Add to mermaid                      :1d
    Functionality added                 :milestone, 2014-01-25, 0d

    section Documentation
    Describe gantt syntax               :active, a1, after des1, 3d
    Add gantt diagram to demo page      :after a1  , 20h
    Add another diagram to demo page    :doc1, after a1  , 48h

    section Last section
    Describe gantt syntax               :after doc1, 3d
    Add gantt diagram to demo page      :20h
    Add another diagram to demo page    :48h
```

### 时序图

```mermaid
sequenceDiagram
    Alice->>John: Hello John, how are you?
    John-->>Alice: Great!
    Alice-)John: See you later!
```

```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>Bob: Hi Bob
    Bob->>Alice: Hi Alice
```

```mermaid
sequenceDiagram
    actor Alice
    actor Bob
    Alice->>Bob: Hi Bob
    Bob->>Alice: Hi Alice
```

```mermaid
sequenceDiagram
    participant A as Alice
    participant J as John
    A->>J: Hello John, how are you?
    J->>A: Great!
```

```mermaid
sequenceDiagram
    autonumber
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
```
`markdown`
```mermaid
sequenceDiagram
    critical Establish a connection to the DB
        Service-->DB: connect
    option Network timeout
        Service-->Service: Log error
    option Credentials rejected
        Service-->Service: Log different error
    end
```

