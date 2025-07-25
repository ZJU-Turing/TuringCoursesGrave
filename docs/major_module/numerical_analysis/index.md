---
abbrs:
    - NA
discussion: TuringCourses/major/numerical_analysis/
latest: https://zju-turing.github.io/TuringCourses/major/numerical_analysis/
---

# 数值分析
<div class="badges">
<span class="badge cs-badge">CS 专业模块-计算机科学</span>
</div>

## 课程学习内容

这门课在简单概念基础之外，主要分为两大板块：解方程，以及插值/近似。与教材章节存在以下对应关系：

- 概念基础
    - 第一章：数学基础
- **解方程**
    - 第二章：一元方程的解
        - 二分法，定点迭代法，牛顿法，也提出了一些加速收敛的方法
        - 本章节都是迭代解法，以定点迭代为分析框架，并进行误差分析
    - 第六章：线性方程组的直接解法
        - 先研究传统的高斯消元法，针对稳定性提出了选主元策略
        - 从多条一元公式的形式，过渡到矩阵标准形式表达，给出基于 LU 分解进行解方程的框架
        - 对特殊类型的矩阵，也有特殊的直接解法
    - 第七章：矩阵代数的迭代解法
        - 其实就是线性方程组的迭代解法，与第六章互补
        - 数学基础：向量/矩阵范数，特征值/特征向量，谱半径
        - 古典迭代方法：Jacobi、Gauss-Seidel 以及松弛迭代
        - 与第二章类似，也进行了误差分析，并给出一种迭代优化的方法
    - 第五章：常微分方程初值问题
        - 常微分的基础理论（截至 2023 秋冬，似乎没学会也不影响考试）
        - 高阶泰勒方法，其一阶形式为欧拉法；Runge-Kutta 法提高精度；隐式法提高稳定性
        - 从单步方法过渡到多步方法，从一元常微分方程过渡到常微分方程组
        - 单独一章讨论稳定性问题
- **插值**/**近似**
    - 第九章：特征值近似
        - 幂法/反幂法/移位幂法，对应模最大/最小/最接近的特征值
    - 第三章：插值与多项式近似
        - 插值方法上，有 Lagrange 插值、Hermite 插值和三次样条插值等
        - 具体计算有 Neville 方法，利用差商记号简化表示
    - 第八章：近似理论
        - 不同于插值，对于近似场景，给定的点可能是不准确的
        - 近似的标准，正交多项式，最小二乘近似
        - Chebyshev 多项式及其应用，但不是最小二乘近似
    - 第四章：数值微分/积分
        - 数值微分相对介绍较少
        - 数值积分，多段复合，再考虑 Richardson 外推引入 Romberg 积分
        - 通过自适应步长、释放选点的自由度等方法，提高积分精度

在解方程板块，除了**精度**，可以看到**收敛性**和**稳定性**也是评估算法的重要标准；而在插值/近似的板块，则可以看到，主要关心的就是**误差**。总体来看，这门课覆盖范围很广，研究的问题也比较基础，学习难度并不小。

## 任课教师

=== "许威威"

    授课：xww 老师就比较正常的计院老师讲课风格，读 PPT 偏多，时不时卡顿，听课与否都是可以的。PPT 也是沿用的 DS 那一套 PPT 风格（都是多年前由陈越姥姥统一制作，比如时不时出现一个大拇指，配上响亮的音效）PPT 基本上可以用来自学，但有些地方可能会觉得莫名其妙，可以结合老师的讲解。

    给分：老师的给分是非常好的，22 Fall 老师公布了平时分的情况，大家平时分几乎都是满分。

=== "黄劲" 

    授课：黄劲老师教学非常有激情，但是相比 xww 老师，难度会更高（他会很贴心地问大家有什么地方没听懂，但是怎么感觉只有我没听懂啊！）。要想跟上他课上的推理，最好熟练掌握此前数学课上所学的知识，以及一点数学素养。PPT 亦是 DS 风格，如果不听课要拿 PPT 来自学，可能会有困难（虽然我听了课也看不懂）。
    
    给分：我推测，中高段会捞（虽然我没捞起来）

=== "童若锋"

    授课：中文授课，各个老师都一样的英文 PPT，讲的还是很清楚的，对知识点有自己的理解并较为明白地解释给我们：为什么要这么做，怎么推导出的、具体例子怎么算，层层深入地阐释。没有纸面作业，课堂上会有小的 Discussion（1-2 题的小测，算分），交上去后会讲解。

    给分：平时分比较求是，不算很捞（有一点），不会乱给你扣分，推测期末卷改的也不是很严。

## 课程教材

*Numerical Analysis 7th*, Richard L. Burden J.Douglas Faires

一本比较老的教材（实际上这本书已经有第十版了，但教材仍然执着于第七版，需要自己买，笔者订了教材也没有拿到）     
书的内容比较多，但部分地方不太清楚，而且和老师上课所讲会有出入。不太建议单纯通过教材自学。    
作业均来自上面的课后题，奇数题答案在书后面，其他的也可以在 Google 上搜索，很多题都是国外 NA 课程的作业。    
xww 老师会发电子版，但期末考试开卷，买一本还是相当有必要的。 

## 分数构成

=== "许威威"

    成绩组成：Lab（36%）+ 期末（40%）+ Quiz（4%）+ 展示（15%）+ 作业（5%）

    * Lab：pintia 上面的 8 个 Lab, 前两三个比较麻烦，因为有些测试点非常恶心，可能需要面向测试点编程。后面的 lab 会比较简单，就是实现书上的算法。老师最开始说的是 lab 布置之后两周之内要完成，不过从最后的结果来看似乎全拖到期末再做也是可以的。可能会查重，但只要不完全一样，好像不会被抓。还是要自己理解了再写，不要直接 CV 网上代码。
        * 这里提供网上一份比较正确的[题解](https://blog.csdn.net/HGGshiwo/article/details/111088392)，但是不要抄袭。
    * 每次课的 PPT 上可能会有若干个 Topics, topics 是需要抢的，如果手慢只有在快期末的时候才能展示了（不过大家都能安排上，不用担心，2024秋冬数量不够，许老师期末又加了几个）。Topic 基本上是让介绍一个算法或者利用讲的算法做拓展，可以回看往年智云查看如何完成，除了用多种插值方法拟合牛头这个 topic 以外最好都要加一些算法分析的内容，工作量不算大，主要就是上网查查资料然后做代码实现。展示后老师或者同学会提问，最后由老师打分。从最后公布的平时分看，只要完成了老师都会直接给满分。可以预先查看往年智云或 PPT 选择自己感兴趣的 Topic 进行展示。
    * Quiz：两次小测，用来点名。回答问题可以抵偿一部分小测分数。
        * 在 2023 秋冬和 2024 秋冬，Quiz 就是签到性质，写错了也能拿满。
        * 在 2024 秋冬以前，回答问题可以加一分，老师说回答了问题下次小测就不用来了（笑）。在 2024 秋冬，回答问题和发现 PPT 错误都能获得所有小测的成绩，即 4 分。
        * 小测数量有微小概率不是两次。
        * 没有提交 Quiz，又比较在意成绩的话，还是要积极点回答老师问题亡羊补牢一下，老师的问题经常没人回答。
    * 作业：每次课后会有几道题作为作业，题不多，但是有的题比较麻烦，需要借助 Python 或者其他的计算工具，否则计算器不知道要按多久。
    * 期末：期末开卷，可以带计算器、教材和打印的 PPT. 考试难度不大，蛮多原题，而且计算量远远低于作业题的难度。对于 PPT 上的原理，证明相关的内容基本不涉及，主要考察各种方法的应用。建议带 PPT，因为会出现 PPT 中 discussion 或者例题。

=== "黄劲" 

    <分数构成，可具体介绍各部分，如作业情况、实验内容及形式、考试范围及形式等> 

    黄劲老师不会公布详细的分数构成，按照他的说法是给分是“弹性的”，但大致上和 xww 老师那边是差不多的。下面仅介绍一些和另外两位老师不太相同的地方：

    * 黄劲老师的 Quiz 相当多（共 15 个，严格来说一个 quiz 是一道题目），但难度不大，有些甚至是教材原题，主要用于巩固知识。Quiz 会不定时地在每周课的最后开始，有时没有 quiz，有时会甚至有 2-3 个 quiz。Quiz 的解答需要写在纸上上交。
    * PPT 上给出的教材作业不要求提交，但强烈建议做一下，不然真的期末火葬场了（悲）。
    * 今年（23 级）的期末考试的题型略有变化：客观题部分多了判断题，但客观题和主观题的大致占比没有太大变化。

=== "童若锋"

    成绩组成：Lab（30%）+ 期末（40%）+ Discussion（18-20%）+ 展示（7%）+ 问答（3-5%）
    
    * Lab：pintia 上面的 8 个 Lab，测试点比较难过，有时候基本看别人代码写出来的，却奇怪地通过不了一些测试点。据说会查重，但只要不完全一样，好像不会被抓。
    * 展示：根据老师给的 Research Topic 做 PPT 解释原理/推导过程/自己代码的实现结果，可以看智云的往年展示，一半互评一半老师评。
    * Discussion：其实就是小测，也用来点名。一般是一个刚刚学的知识点的小题目，交上去写了名字就有60%。不难，可以在历年整合好的PPT找到答案。最好还是理解，不要有答案就硬抄。
        * 学完一部分（总共三部分：解方程、插值和积分、常微分）会有一次阶段性测试，占比大一点，题目类型与期末类似，是好的复习机会。试卷会发下来讲，应该能找到历年的。
    * 回答一次问题可以加一分，发言困难症没凑齐（哭）
    * 作业：不同于其他老师，没有纸质作业，事少。
    * 期末：开卷，建议带上 PPT，感觉教材其实可有可无，主要内容和方法都在 PPT 上，顺序与教材不同，没看过那本厚厚的教材会很难找。当然一份自己整理好的纸质笔记就更好了。考的东西不难，计算量较大，题目不一定直接告诉你用什么方法，而是委婉地说某种方法的特征，所以需要理解各个方法的使用原因。


## 参考资源

- [QJJ 的学期回顾](https://www.cc98.org/topic/5511167)（内有回忆卷，个人和部分学长的建议）
- [QJJ 的资源 repo](https://github.com/HobbitQia/ZJU-Courses-Resources/tree/master/%E6%95%B0%E5%80%BC%E5%88%86%E6%9E%90(NA)) （内有作业 1-13 反馈（由许威威老师在期末时公布）内有作业部分易错点的讲解；2022-2023 FALL 期末回忆卷；所有 PPT 整合在一起的pdf）
- [ZhouTimeMachine 的笔记](https://zhoutimemachine.github.io/note/courses/numerical/analysis/)


## 学习建议

计院数值分析涵盖内容比较广，实际上涉及了数院数值分析、数值代数、微分方程数值解三门课的内容，因此想要深入贯通难度还是比较大。

考试范围是可能超出作业题范围的，所以平时不能只做作业涉及的内容，例如 2023 秋冬 Gaussian Quadrature 一节并没有布置作业，但是考试却考到了。同时不看 PPT 只看教材也是不够的，教材和 PPT 有较大的交集，但是两者都有对方没有的内容，并且有的小节的讲解逻辑也不同，面向考试出发的话可能基于 PPT 更好，希望贯通的话可以两者结合着看。

考试推荐还是买一个高级计算器（比如卡西欧），功能强大一些，掌握计算器直接求矩阵逆、直接解方程等技巧还是可以省下不少考试时间。考试题目比较灵活，还是考察对知识的理解，所以不要面向作业题、历年卷过拟合了，例如 24 年期末就考了外推法推导二次导数的近似公式，许多同学考场现场学习，还是推荐平时多多思考，跟上课程节奏规律学习，以免期末火葬场。
