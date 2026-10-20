# Fahreigenschaften I · Reifenkräfte · P11–P20
# 德中对照逐页教学：变形、刚度、面压与滚动阻力

来源：`FE_1_Kap_2_Reifenkräfte_WS26_27(2).pdf`，124 页；本批严格对应 PDF 序号及原页脚 11–20。课程：Universität Stuttgart，Institut für Fahrzeugtechnik Stuttgart；页脚署名 Dr.-Ing. Dipl.-Math. Jens Neubeck，日期 12.10.2026。核对日期 2026-10-20。

原文件 SHA-256：`00bafe73bfbbb48bd0b3e10d62b8490058b727639036c1f9558b8312b9948f29`。本批完成文字与静态页图核对。PDF 上的播放图标不等于已观看原 PPT 动画；本笔记不推测动画内容。

“课件内容”对应可见原文与图；“教学补充”包括通俗解释、模型、例题和德语复述句，不冒充原页公式。本批原图包含曲线、变量和 P17 的位移相加标注，但没有以下补充模型的完整推导。全部数值例题都是另设条件。

## 本批知识路线

| 页 | 原页主题 | 学习目标 |
|---|---|---|
| P11 | Globale Reifen-Deformationsmechanismen | 识别四类整体变形，并读出载荷—变形曲线 |
| P12 | Bauteil- bzw. Materialsteifigkeiten | 区分不同刚度及其自变量、单位 |
| P13 | Grundsteifigkeit und Reifeninnendruck | 理解结构和内气压都影响弹簧刚度 |
| P14 | Normalkraft und Latschfläche | 理解轮载增加时接地面积增大 |
| P15 | Schubspannungsverteilung / lokale Deformation | 将整体结构、面压、局部剪切联系起来 |
| P16 | Stauchen, Scheren und Gleiten | 区分压缩、剪切与接触滑动 |
| P17 | 花纹块通过接触区的连续图 | 理解剪切阶段、滑动阶段和位移分解 |
| P18 | unsymmetrische Flächenpressung / e_R | 理解面压偏心如何形成阻滚力矩 |
| P19 | Fahrgeschwindigkeit und Flächenpressung | 读懂速度提高时入口峰值的变化 |
| P20 | Radlaständerungen und lokale Flächenpressung | 理解轮载改变面积，也改变面压分布 |

## P11 · Globale Reifen-Deformationsmechanismen — 整体轮胎变形机制

### 课件图像逐列解释

原页来源标注：Yukio Nakajima, Advanced Tire Mechanics, 2019。四列各有一幅上方变形示意和一条下方响应曲线。实线、虚线用于对照几何状态，不是两个轮胎型号。

| 原图列名 | 中文 | 上方图意 | 下方横轴 | 下方纵轴 |
|---|---|---|---|---|
| vertikal | 垂向变形 | 轮胎结构在垂向载荷下发生位移和变形 | vertikale Verschiebung：垂向位移 | vert. Kraft F_N：法向力 |
| lateral | 侧向变形 | 胎冠／接地部分与轮辋发生侧向相对偏移 | laterale Verschiebung：侧向位移 | lat. Kraft F_S：侧向力 |
| Rotation | 绕车轮轴线的转动变形 | 轮胎内部示意线弯曲，体现轮辋与外部结构间的相对扭转 | longitudinale Verschiebung：纵向位移 | long. Kraft F_L：纵向力 |
| Torsion | 绕近似路面法向轴的扭转 | 俯视轮胎轮廓发生角度差 | Torsionswinkel：扭转角 | Torsionsmoment M_z：扭矩 |

**特别注意 Rotation 那一列：** 上图画的是转动形式，下图明确用“纵向位移”作横轴。不能仅凭 Rotation 字样把它读成“纵向力对转速的关系”。Torsion 列才是扭矩对扭转角的示意。

### 曲线怎么读

垂向曲线整体上随位移增加而增加，末端有弯曲；侧向、纵向和扭转响应曲线在初始区较陡，随后斜率减小，后两者还示意轻微回落。**原图没有数值刻度**，因此只能读出定性非线性，不能从图上报出刚度数值、峰值力或具体滑移率。

教学补充：小变形时可在工作点附近近似线性；变形增大后，接触状态、有效几何及滑动区域等因素会使响应偏离直线。原页未将每段曲线分别归因，不能说某个拐点必然对应某个特定工况。

### 教学补充公式：刚度是曲线斜率

$$c_z=\frac{\partial F_N}{\partial z},\qquad c_y=\frac{\partial F_S}{\partial y},\qquad c_\psi=\frac{\partial M_z}{\partial\psi}.$$

位移刚度单位为 N/m；转角刚度单位为 N·m/rad。这里的正方向、固定条件和工作点需要另定。局部切线刚度与从原点连线得到的割线刚度可以不同。

**汽车实例：** 压过凸起主要激发垂向响应；稳态转弯有侧向结构挠曲；驱动和制动转矩会使轮辋与胎冠间出现相对变形；停车转向时，接触区对转向扭转产生阻抗。它们不是四种彼此隔绝的轮胎，而是同一只轮胎的不同响应方向。

**DE 复述：** Ein Reifen kann sich vertikal, lateral, in Umfangsrichtung und um die Hochachse verformen.

**本页抓手：** 读曲线先读横轴和纵轴，再看斜率；Rotation 不等于“转速”。

## P12 · Steifigkeiten — 刚度的分类

### 课件原文与译意

“Die elastischen Deformationen sind durch die Bauteil- bzw. Materialsteifigkeiten bestimmt.”

弹性变形由部件刚度和材料刚度决定。这里不仅指胶料本身：胎体、带束层、胎侧以及几何布局也影响部件响应。

原页依方向和取向列出六类，全部保留：

| Deutsch | 中文 | 教学上首先要问什么 |
|---|---|---|
| Vertikalsteifigkeit (auch exzentrische Steifigkeit) | 垂向刚度（原页亦称偏心刚度） | 法向力随垂向相对位移如何变化？ |
| Längssteifigkeit | 纵向刚度 | 自变量是纵向位移，还是后续定义的纵向滑移？ |
| Schräglaufsteifigkeit | 侧偏刚度 | 侧向力随侧偏角如何变化？ |
| Seitenkraftsteifigkeit | 侧向力刚度 | 在本处结构变形语境下，侧向力随侧向位移如何变化？ |
| Torsionssteifigkeit (um Hochachse) | 绕竖轴的扭转刚度 | 绕该轴的力矩随扭转角如何变化？ |
| Sturzsteifigkeit | 外倾刚度 | 外倾角改变时，相关侧向力响应怎样变化？ |

本页没有给出这些刚度的符号定义、测量方法或单位。以下是帮助区分的常用局部线性表达，精确定义必须与教授后续约定核对，不能把这些表达写成该页的逐字公式：

$$\Delta F_S\approx C_\alpha\,\Delta\alpha,\qquad \Delta F_S\approx c_y\,\Delta y.$$

第一式的 $C_\alpha$ 通常用 N/rad；第二式的 $c_y$ 用 N/m。它们的自变量不同，即使中文都含“侧向”，也不是同一参数。侧偏角描述车轮指向与其速度方向的差异；侧向位移描述结构相对偏移。

对外倾的局部响应也可定义 $C_\gamma=\partial F_S/\partial\gamma$，单位 N/rad，但需固定其他条件、确认正方向。不要把侧偏角与外倾角合成一个角。

“Längssteifigkeit”也需要看上下文：若写 $\partial F_L/\partial x$，单位 N/m；若后续以无量纲纵向滑移为自变量，单位则为 N。名称相同不能代替自变量定义。

**单位算例：** 若教学设定 $C_\alpha=60000$ N/rad，线性区角增量为 $1^\circ=\pi/180$ rad，则侧向力增量约 1047 N。将数字 1 直接代入以 rad 为单位的公式，会产生约 57.3 倍的错误。符号方向需按坐标约定决定，本例计算大小。

**汽车实例：** 两只轮胎可能具有接近的垂向刚度，却有不同的侧偏刚度；乘坐舒适性接近，不等于转向响应完全相同。

**本页抓手：** 每个刚度都要回答“什么力或力矩，对什么位移、角度或滑移求斜率”。

## P13 · Struktur und Luftfeder — 结构与空气弹簧贡献

### 课件内容

**DE：** Ein Luftreifen besitzt durch seinen strukturellen Aufbau eine Grundsteifigkeit; der Luftinnendruck erhöht zusätzlich die Federrate.

**中：** 充气轮胎本身的结构提供基础刚度，内部气压又会提高其弹簧刚度。

### 原图逐项读法

图源仍为 Nakajima。横轴 Reifeninnendruck 是轮胎内气压，纵轴 Federsteifigkeit 是弹簧刚度。示意直线从一个大于零的截距开始，并随内气压上升。右侧括号将总体示意分为 Struktureller Anteil（结构贡献）和 Luftfeder Anteil（空气弹簧贡献）。

**关键区别：** 这幅图纵轴是“刚度”，不是“载荷”；不能读成“胎压增加必然使车重增加”。零气压端的截距说明结构有基础刚度，不表示失压轮胎仍能正常安全行驶。

### 教学补充模型

为了复述图意，可写：

$$c_{z,\mathrm{eff}}\approx c_{\mathrm{str}}+c_{\mathrm{air}}(p_i).$$

在有限范围内还可示意 $c_{\mathrm{air}}\approx k_p p_i$。这只是解释原图的分解，不是精确可独立测量、互不耦合的两根弹簧；实际充气也会改变结构预应力和几何状态，不能据示意图推断全范围严格线性。

**汽车实例：** 在其他条件近似相同的情况下，提高胎压常使轮胎垂向响应更硬，经过接缝的冲击感可能增强。但这里没有提供任何车辆的推荐胎压，也没有证明“越高越好”。

**DE 复述：** Die Reifensteifigkeit entsteht nicht allein durch die Luft, sondern auch durch die Struktur.

**本页抓手：** 结构提供基础，充气改变刚度；刚度、压力和载荷是不同物理量。

## P14 · Normalkraft und Latschfläche — 法向载荷与接地面积

### 课件内容

“Erhöhung der Normalkraft bewirkt eine Erhöhung der Latschfläche.”

法向力增大，使接地印痕面积增大。

### 原图怎么读

上方两幅同类轮胎照片对照受载状态，右侧绿色向下箭头更长，表示更大的法向载荷。下方接地轮廓相应变大。这里的箭头是定性示意，不是按比例标定的载荷数值。下方俯视接触图不是另一只独立轮胎。

### 教学补充：从总载荷到接触区域

轮胎是可变形结构。受载增加时，它通过进一步变形改变接触区域，使更多区域参与承载。其基本关系仍为：

$$F_N=\int_A p(x,y)\,\mathrm dA=\bar p\,A.$$

**课堂式算例：** 假定平均面压近似保持 250 kPa，轮载从 4000 N 增至 5000 N，则估计面积从 160 cm² 增至 200 cm²。这个算例额外假设平均面压不变；原页没有保证该假设，P20 还会说明面压本身也会改变。

**汽车实例：** 满载与空载时，同一轮胎的受载和接地形态通常不同；制动时前后轴载荷转移，也会使各轮接触区重新调整。不能只记总车重而忽略各轮实际轮载。

**本页抓手：** 轮载增加会改变接地面积；不能据此断言面积与载荷在所有条件下严格成正比。

## P15 · Von global zu lokal — 从整体结构到花纹块剪切

### 原页四项内容逐条解释

| 原文要点 | 德中术语 | 中文解释 |
|---|---|---|
| 整体变形显著影响接地面的形状和面压 | globale Deformation; Reifenaufstandsfläche; Flächenpressung | 先看整个轮胎怎样受载、怎样接触道路 |
| 胎面中形成剪切应力分布，花纹单元受剪 | Schubspannungsverteilung; scheren | 接触力在空间中分布，不是集中在一个点 |
| 花纹通过接触区时，先黏着，逐渐受剪，随后可能在变形状态下滑动 | haften; deformieren; gleiten | 接触区内一个材料单元的历程有先后阶段 |
| 花纹单元在接触区内的变形称为局部变形 | lokale Deformation | 这是 P10 所说 lokal 的具体对象 |

“haften”在这里是接触运动意义的黏着：该处橡胶底面与道路没有局部相对滑动。它不是说上下所有材料点都不动，也不是专指分子黏附这一种摩擦机理。

### 教学补充：一个花纹块为何越走越斜

设花纹块底部暂时黏着路面，而顶部随带束／胎冠运动，两者相对位移逐渐积累，花纹块便剪切变形。局部可维持的接触力有限；当剪切要求超过可维持的黏着能力时，底面开始相对道路滑动。

原页叙述的是典型示意过程。并非所有花纹块在每种工况下都必须出现明显滑动，也不能把每个工况的接触区一律切成固定比例的黏着区与滑动区。

```mermaid
flowchart LR
    A[整体结构变形] --> B[接触形状和局部面压]
    B --> C[花纹块受压与剪切]
    C --> D[局部黏着或滑动状态]
    D --> E[分布切向应力]
    E --> F[轮胎纵向和侧向合力]
```

这是本笔记自制逻辑图，不是原页实验框图。

**汽车实例：** 温和制动时，部分接触区仍可黏着传力，同时橡胶块发生剪切；提高制动需求会改变剪切量和局部滑动范围。轮胎力并非只有“完全无力”与“整胎打滑”两个状态。

**本页抓手：** 局部黏着与橡胶弹性剪切可以同时存在。

## P16 · Stauchen, Scheren und Gleiten — 压缩、剪切、滑动

### 原图四幅状态，按从左到右阅读

图源：Michelin, Der Reifen – Haftung。

| 原图标签 | 中文 | 图形变化 | 物理判据 |
|---|---|---|---|
| Gummielement Ausgangslage | 橡胶单元初始状态 | 初始高度和轮廓 | 作为对照状态 |
| Gummielement gestaucht | 被压缩 | 向下 F_N 箭头，块体变矮并鼓胀 | 法向压缩形变 |
| Gummielement gestaucht und geschert | 被压缩且受剪 | 保持法向载荷，顶部有水平力，块体倾斜 | 上下表面发生相对位移；底面仍可黏着 |
| Gummielement gestaucht, geschert und gleitend | 被压缩、受剪并滑动 | 块体倾斜，底部接触位置相对原位置改变 | 底面与道路发生相对运动 |

虚线轮廓帮助比较前后形状。不能只看到块体倾斜就说它已经滑动：第三幅已经受剪，但第四幅才明确增加 gleitend。

### 教学补充：三个词对应三个不同问题

- **Stauchen**：高度怎样变化？对应法向压缩。
- **Scheren**：上面相对下面偏了多少？对应内部剪切形变。
- **Gleiten**：底面相对道路是否移动？对应接触滑动。

简化弹性模型可写 $\tau\approx Gu/h$，其中 $u$ 是上下表面的切向相对位移，$h$ 是高度，$G$ 是剪切模量。$u\ne0$ 并不自动推出底面滑动；它首先表示花纹块有剪切形变。

还可用局部库仑式近似说明黏着能力上限：$|\tau|\lesssim\mu p$。这是教学简化，橡胶摩擦还依赖状态，原页没有给出一个通用常数 $\mu$。切勿把两个补充关系当作完整轮胎模型。

**汽车实例：** 像按住橡皮擦底面，再推它的上部：可以先让它变斜，推得更强才开始在桌面上滑。胎面单元也可有相似的“先形变、后局部滑动”过程。

**本页抓手：** 形变发生在材料内部，滑动发生在接触界面；二者不能用同一个词代替。

## P17 · Ein Profilelement durchläuft den Latsch — 花纹单元通过接地印痕

### 原图左侧：从上到下追踪黄色标记

图源仍为 Michelin。左侧五幅连续示意用黄色标记帮助追踪同一个花纹单元。原图旁白依次出现：

1. **Der Block kommt in Kontakt mit der Straße.** 花纹块与道路接触。
2. **Der Block wird unter der Radlast gestaucht.** 花纹块在轮载作用下被压缩。
3. 接触过程继续，形状和位移继续演化。
4. **Es tritt Scherung ein.** 出现剪切。
5. **Es tritt Schlupf ein und der Block rutscht durch.** 出现局部滑动，花纹块滑过道路。

不能把这五幅看成五种不同胶料，它们是在说明一个单元随时间经历的状态。

### 右侧图：方向与阶段

图中 $v_{Fahrzeug}$ 箭头向右，表示车辆运动方向；$\omega r$ 箭头向左，标为 Radumfangsgeschwindigkeit（车轮圆周速度），用于表现轮胎材料相对轮心的周向运动。两根箭头不是同一参考点在同一参考系内的两个相反绝对速度。

在这张示意中，接地单元从右侧进入，随材料经过接触区向左侧离开。右侧标为 Scherphase（剪切阶段），左侧标为 Schlupfphase（滑动阶段）。注意：材料在接触区中的流动方向与车辆前进方向不同，不能看见车向右开就把图左端认作入口。

原图标出总相对位移由 Schlupfweg（滑动距离）和 Scherlänge（剪切位移）组成，写有 $l_s+l_{Sch}$。这是**两个长度相加**，不是“滑移率与长度相加”。后续讲义如果另定义无量纲 Schlupf，必须与这里的位移尺度区分。

### 教学补充：位移如何分成两部分

用本笔记自定符号写：

$$u_{\mathrm{rel}}=u_{\mathrm{el}}+s_{\mathrm{slide}}.$$

左边是顶部相对道路参考位置的总位移；右边分别是材料弹性剪切位移、底面相对道路的滑动距离。局部黏着阶段可以 $s_{slide}=0$ 而 $u_{el}>0$；进入滑动阶段后，两部分都可存在。

**算例：** 顶部相对道路参考位置共移 5 mm，其中块体剪切贡献 3 mm，则底面滑动距离是 2 mm。不能把 5 mm 全部叫作接触滑动距离，更不能把它直接称为 5% 滑移率。

**汽车实例：** 看轮胎宏观轮速与车速的差，可以描述整体滚动状态；要解释胎面局部如何传力，还需看一个块体在接触区内有多少弹性剪切、多少界面滑动。宏观量与局部状态有关，但不是一一同义。

**本页抓手：** 跟着同一个材料单元读图；总位移可包含“材料变形”和“界面滑动”两部分。

## P18 · Unsymmetrische Flächenpressung — 不对称面压与滚阻力臂

### 课件内容与术语

| Deutsch | 中文 |
|---|---|
| Eintritt in die Kontaktfläche | 进入接触区 |
| unter der Wirkung der Normalkraft gestaucht | 在法向力作用下被压缩 |
| unsymmetrische Flächenpressungsverteilung | 不对称的接触压强分布 |
| resultierende Normalkraft greift außermittig an | 合法向力的作用线偏离中心 |
| Hebelarm der rollenden Reibung e_R | 滚动阻力的力臂 e_R |
| siehe Rollwiderstand | 参见后续滚动阻力内容 |

### 原图怎么读

本页车辆速度 $v_F$ 指向左，图中轮胎向左滚动。因此本图左侧是前方，与 P17 的车辆向右示意不同。绿色小箭头代表路面法向作用的分布，较大的绿色向上箭头表示其合力；灰色／黑色向下箭头表示轮心处的法向载荷示意。不要把两个 F_N 当成“同一作用点上可任意互消的一对力”。

绿色合力作用线在轮心竖线的左侧，即朝本图行驶前方偏移；两条作用线之间的水平距离是 $e_R$。**e_R 是长度，不是角度，也不是已经无量纲化的滚阻系数。**

### 教学补充：偏心怎样产生阻滚力矩

法向力若通过轮心正下方，单由该力不会对轮心形成这种偏心力矩。作用线前移后，就产生一个阻碍当前滚动方向的力矩，其大小可表示为：

$$M_R=F_N e_R.$$

如果再以有效滚动半径 $r$ 把该力矩换算为等效阻力大小：

$$F_R=\frac{M_R}{r}=\frac{e_R}{r}F_N,\qquad f_R=\frac{F_R}{F_N}=\frac{e_R}{r}.$$

这些是为解释原图补充的大小关系，符号正负和有效半径定义需按后续课程约定。$M_R$ 单位 N·m，$e_R,r$ 单位 m，$f_R$ 无量纲。等效阻力是另一种描述方式，不能在同一平衡式中把它和原偏心力矩不加处理地重复计入。

**算例：** 设 $F_N=4000$ N、$e_R=3$ mm、$r=0.30$ m，则 $M_R=12$ N·m，$F_R=40$ N，$f_R=0.01$。这些数字不是从原图读出的。

教学解释：真实轮胎变形与恢复中的耗能、动态响应等会与这种不对称分布关联。原页着重给出几何作用线和滚阻入口，不在这里推断全部损耗来源。

**汽车实例：** 车辆在平路松开驱动后仍逐渐减速，滚动阻力是阻力来源之一；不能把全部减速都归于空气阻力，也不能把滚阻等同于轮胎在路面上整块滑动。

**本页抓手：** 不对称分布使合力偏心；偏心距离乘以力得到阻滚力矩。

## P19 · Geschwindigkeit und Druckverteilung — 速度与接触面压

### 课件内容

“Eine Erhöhung der Fahrgeschwindigkeit erhöht die Flächenpressung am Latscheingang.”

行驶速度提高，会使接地印痕入口处的接触面压增大。

### 原图坐标与曲线

- 横轴 Latschlänge：沿接地印痕长度方向的位置；不是时间轴。
- 纵轴 Flächenpressung：接触面压；不是整胎合力。
- 图左侧 Eingang 是入口，右侧 Ausgang 是出口。
- 灰色曲线较平坦，绿色虚线在入口附近出现较高峰值；速度 $v$ 的箭头指示这种变化趋势。
- 后半段面压曲线相应有所改变，图像强调分布形状变化。

这张图没有速度、压力或距离的数字刻度，不能据此计算“增加 10 km/h 后压力增加多少”。入口在图左，只是该页分布图的轴向安排，不能机械套用到 P17 的轮胎侧视运动方向。

### 教学补充：局部峰值不是总载荷

若用沿接触长度的**单位长度载荷** $q(x)$ 表示宽度积分后的压力分布，则：

$$q(x)=\int p(x,y)\,\mathrm dy,\qquad F_N=\int q(x)\,\mathrm dx.$$

$q$ 的单位是 N/m，$p$ 的单位是 N/m²。不能不考虑宽度，就把原图的“面压—长度”曲线面积直接当成 N；若假定有效宽度 $b$ 一致，才可近似写 $F_N\approx b\int p(x)\,\mathrm dx$。

在轮载固定条件下，局部入口峰值增大不意味着总载荷也同比增加，还要看整个二维分布如何调整。合力位置则取决于分布的一阶矩；这也连接到 P18 的偏心距离。

教学解释：速度变大时，材料单元进入接触区、受压和恢复的时间尺度改变。轮胎具有动态和黏弹性响应，入口处可呈现不同面压。原页只给定性趋势，没有把曲线变化唯一归因于一个材料参数。

**汽车实例：** 同样轮载下，低速与高速滚动的局部接触状态可以不同，不能把静态压印纸上的图形当成所有速度下的完整接触状态。

**本页抓手：** 入口峰值、全域积分和合力作用位置，是三个不同信息。

## P20 · Radlast und lokale Flächenpressung — 轮载不仅改变面积

### 课件内容

**DE：** Radlaständerungen beeinflussen neben der Größe der Aufstandsfläche auch die lokale Flächenpressung erheblich.

**中：** 轮载变化除了改变接地面积，也会显著改变局部接触面压。

图源标注：Thomas Mathews Vayalat, Tire Contact Patch Characterization through Finite Element Modeling and Experimental Testing。这里只记录课件的可见归属，未额外访问该文献全文。

### 原图怎么读

左、右各是一幅有花纹沟槽的接触面彩图，箭头 Radlasterhöhung 指向右，表示右侧对应更高轮载。颜色分布在不同花纹块内不均匀，局部出现不同强度的颜色区域；右侧的接触轮廓与分布发生改变。

按这类图常用配色可以把暖色理解为较高、冷色为较低压力的示意，但**原页未展示色标、单位或两图的归一化设置**。因此不能报出红色处多少 MPa，也不能仅凭红色区域面积，精确计算两图的峰值比。花纹沟槽的白色间隔也不能简单当成有胶料却测得零压的完整平面。

### 与 P14 的区别

P14 的重点是“接触范围扩大”；本页进一步说明“扩大后的区域内部也重新分配载荷”。不是把原先一张均匀压力图按比例放大就完事。

$$F_N=\int_{A(F_N)}p(x,y;F_N)\,\mathrm dA.$$

这是教学整理：载荷改变时，积分区域 $A$ 和被积分的分布 $p$ 都可以改变。它不是额外一条独立的材料定律。

**汽车实例：** 弯道中外侧轮载增加，接地面积和各花纹块受压都可能调整。不能仅凭面积更大就推出“该轮可提供的侧向力与轮载严格同比增加”；要回答实际侧向能力，还需后续轮胎力—滑移模型和载荷效应。

**本页抓手：** 面积是几何信息，面压是分布受力信息；两者都随轮载变化。

## 德中术语速查

| Deutsch | 中文 | 不要混淆 |
|---|---|---|
| Verschiebung | 位移 | 不是速度 |
| Steifigkeit / Federrate | 刚度／弹簧刚度 | 不是载荷，也不是材料强度 |
| Grundsteifigkeit | 基础刚度 | 不等于无气压下正常使用能力 |
| Schräglaufsteifigkeit | 侧偏刚度 | 不等于侧向位移刚度 |
| Schubspannung | 剪切应力 | 单位 Pa，不是 N |
| Stauchung | 压缩变形 | 不等于切向剪切 |
| Scherung | 剪切变形 | 不必然已经界面滑动 |
| Haften | 黏着接触状态 | 不意味着材料内部不变形 |
| Gleiten / Rutschen | 滑动 | 与纯弹性剪切分开 |
| Schlupfweg | 滑动距离 | 不是无量纲滑移率 |
| Flächenpressung | 接触压强／面压 | 不等于轮胎内气压 |
| Radlast / Normalkraft | 轮载／法向力 | 不是接触面积 |
| außermittig | 偏心地 | 对应合力作用线的位置 |
| Hebelarm e_R | 滚阻力臂 | 有长度单位，不是 f_R |

## 本批补充公式与使用边界

| 用途 | 模型或关系 | 边界 |
|---|---|---|
| 刚度 | 力／力矩对位移／角度的局部导数 | 指定工作点、固定量和正方向 |
| 侧偏刚度 | ΔF_S ≈ C_α Δα | 小角线性范围；N/rad 与 N/°不可混用 |
| 充气贡献 | c_eff ≈ c_str + c_air(p_i) | 示意分解，不承诺结构与空气完全解耦 |
| 合法向力 | F_N = ∫p dA | 不是 p_i 乘面积的无条件精确式 |
| 局部剪切 | τ ≈ Gu/h | 小形变线弹性近似 |
| 局部接触限值 | abs(τ) ≲ μp | 教学摩擦近似，不是完整橡胶模型 |
| 位移分解 | u_rel = u_el + s_slide | 两项均为长度，符号按所选方向 |
| 滚阻力矩 | M_R = F_N e_R | 大小关系；不要与等效阻力重复计入 |
| 等效滚阻 | F_R = M_R/r；f_R = e_R/r | 指定有效半径；f_R 无量纲 |
| 一维积分 | F_N = ∫q dx；q = ∫p dy | 分清 N/m 与 N/m² |

## 闭卷自检：尚未作答，不附答案

建议先合上笔记，再用自己的话回答。题目范围为 P11–P20，属于概念辨析和简短计算，未规定考试用时。

1. P11 的 Rotation 列，下方曲线的两个坐标分别是什么？为什么不能把它解释为纵向力随转速变化？
2. C_α 的单位若是 N/rad，而另一个 c_y 的单位是 N/m，它们分别对什么量求变化率？
3. 花纹块已经倾斜，能否仅凭这一点断言它在路面上滑动？解释判断依据。
4. 用自己的话说明为什么轮载增加后，不能只把接地面积按比例放大而保持局部面压完全不变。
5. 给定 F_N=3500 N、e_R=2 mm、r=0.28 m，求滚阻力矩和等效滚阻力大小，写出单位。
6. 入口面压峰值升高，是否一定意味着该轮总法向力增加？请说明还需要看什么。

## 状态与续学断点

- 本批 P11–P20 已核对并形成详细讲解；这不等于学生已独立掌握。
- 无学生新作答，不生成分数、错因或 PASS。历史 Karkasse／Stahlgürtel 辨析待复测。
- 下一批从原 PDF P21 起，默认 P21–P30，遇章节边界调整。
- 本次只读取并讲解到 P20，P21–P124 不标为已审阅。
- Operation：`FE-20261020-P11-20-DEZH-01`。
