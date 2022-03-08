
![GitHub last commit](https://badgen.net/github/last-commit/Meng2025/electronics/main)
![Github commits](https://badgen.net/github/commits/Meng2025/electronics/main)
![no problems](https://badgen.net/badge/no%20problem/(maybe)/red)

*感谢访问我的学习笔记。*

*如果是在GitHub看到这些内容，那么可以前往[独立网页](https://xu.yumeng.website/electronics/)获得更好的浏览体验。*

*如果觉得我的笔记内容对您有帮助，那我会感到非常开心。*

最重要的

**如果我在内容上有理解错误，或者表达不严谨、符号不规范的地方，还请不吝指正。**

<img src = "./images/wechat.png" width="100px" align="right">

我的邮箱地址：[*m@njust.edu.cn*]()

或者扫描右侧二维码添加我的微信交流

---

目前断断续续地在整理模拟电路部分。

**这个笔记本将要整理的内容：**
- [ ] 基本元件与电路基本定理（电路分析初步）
  - [ ] 电路模型、纯电阻电路、电路定理
  - [ ] 储能元件一阶二阶电路瞬态分析*（控制实例）、
  - [ ] 交流电路、正弦稳态电路、三相电路*
  - [ ] 半导体器件：二极管、晶体管、场效应管

- [ ] 模拟电路基础*
  - [ ] 信号放大：晶体管放大、场效应管放大、集成运放放大
  - [ ] 控制思想：频率响应、反馈放大（自控精髓，模电核心）
  - [ ] 实用电路：信号运算、波形发生、信号转换、功率放大、直流电源

- [ ] 数字电路
    - [ ] 基础知识：数制码制和布尔代数、逻辑门
    - [ ] 组合逻辑电路分析和设计，常用模块：编码器、译码器、加法器
    - [ ] 存储电路：锁存器、触发器、寄存器、存储器
    - [ ] 时序逻辑电路，常用模块：移位寄存器、计数器、脉冲发生

- [ ] 数字和模拟
  - [ ] 数字电路里的模拟因素：门电路实现、CMOS和TTL、传输线问题
  - [ ] 模拟与数字的转换
  - [ ] 常见模数混合电路：施密特触发、单稳态、多谐震荡、555定时器、锁相环、伪随机比特

- [ ] 微机原理与MCU
  - [ ] 8086微处理器
  - [ ] MCU最小系统外围电路

- [ ] 高频技术、低功耗设计、传感器与检测技术

- [ ] 电路系统开发

---

## 简单介绍

这个笔记本的结构基本上参考了The Art of Electronics这本书，内容上参考了电类专业的经典教材。

整理这个笔记实际上也是我自己建立整个电子学体系的过程，本科的一门一门独立课程像是一块块砖，现在我拿这些砖参考着The Art of Electronics这座大厦的蓝图，盖一栋属于自己楼。

电路分析这门课建立起对电的直觉，模拟电子技术是电子学里闪闪发光的部分，数字电子技术的主线内容是封装好的逻辑电路，反而弱化了电的属性，难度要比模拟电路低不少。这三部分理解透彻以后，再学其他电类的课程也会轻松许多。

电路分析，或者电路，是在大二上学期开的课，学完基础数学物理课程后的第一门专业基础课。对于学电类的同学来说，也是建立“电”的基本概念基本思维和电的直觉的一门课，所以包含的内容很广泛。最开始的是衔接高中的基本欧姆定律、基本电阻电路分析开始，引出了电路基于基尔霍夫定律（“路”是对“场”的简化，电机电磁场的磁路）的四大分析方法以及电路定理。电路分析里的运算放大器内容是一个铺垫，或者说初次露脸，使得在模拟电路中见到这个东西不会显得太难接受，当然比如“虚短”、“虚断”等分析方法是普适的。一二阶电路是自动控制原理的一个实例（类和对象），是将来对电系统进行控制的直觉的来源，**响应**这个词在这里就已经有了。实际上，状态方程在这里也出现了（邱关源5版），只不过标了*，这可是现代控制理论里面一个作为基石的概念。后面的正弦电路分析、三相电路是电机、电力系统等课程的基础（电力系统我不是很了解，虽然我是电气专业，但是学的一塌糊涂）。

模拟电路的书还是挺厚的，其中最核心的两个事情：**放大**和**反馈**。放大是模拟电路里面要解决的首要问题，三极管、场效应管单管放大电路，对于一级放大倍数不够用还有多级放大电路，为了解决温漂等问题改进出差分放大电路，分立元件往往又乱又容易出问题不好使，于是封装成了模块（集成运放）。**为了让放大倍数更加稳定，受外界干扰更小，就引进了反馈**。在分析反馈之前，模电教材插入了一章频率响应，这也是不得已而为之，频率分析是自动控制原理里面的一个重要分析手段，用来分析引入负反馈的闭环控制系统，所以频率响应之后才好研究电路里面的反馈。研究反馈系统的稳定性、稳态性能（放大倍数）。模拟电路确实不容易学明白，因为模拟电路不仅仅是在讲电路，难在**反馈**。反馈可是自动化专业要花至少1学年去领会的东西。我本科是电气工程专业，模拟电路课程开在自动控制原理前面，当时的模电是咬着牙学完的，现在熟悉了自动控制原理的一些思想回头来看模拟电路，还是能发现到模拟电路里处处体现渗透着自动控制原理的思维方法。比如说用深度负反馈去减弱非线性因素的影响的输出控制思路，可以很容易在模拟电路里面找到实例。至此模电的理论部分就结束了。剩下的都是应用了，基于叠加原理的运算，波形处理，以及信号能量比较大的情况下（功率放大）的一些细节问题。还有和自控结合也紧密的一个应用，直流电源，本质是在用输出电压做反馈去自动调节串入回路的电阻使得输出电压跟随给定值而不受负载的影响。

我个人觉得数字电路主线内容的学习并不需要模拟电路的基础，简单的了解放大器件，明白我们需要它工作在个什么状态以后实际上就不影响后续挺有意思的内容的展开了。甚至不懂放大元件，将封装好的逻辑门作为最底层也不影响主线内容的进行（逻辑门是封装好的模拟电路，对外展示为输入输出引脚）。这部分内容是计算机硬件的前置内容，学完这部分实际上已经有设计一个简单CPU的潜力了。

现在实用电子系统几乎都是模拟+数字，因此也有必要了解一下模数之间的联系以及信号转换。现在的实用电子系统的核心微处理器或者微控制器也是一个很重要的内容，所以这部分再电子学里也很合理，实际上数字电路和微机原理也是计算机技术里的知识。

最后这个笔记里还包括了高频、检测、电子系统开发、低功耗等一些内容。

---

除了处理信息的电路，还有处理功率的电路，功率电路原理上和模拟电路有相通的地方，但也有自己的一些成体系的理论和技术，其中有随着电机控制一通发展起来的电力电子技术，这一整套设备里拿掉作为负载的电机，剩下的功率变换部分便是电力电子技术关注的内容。负载不仅仅可以有电机，任何用电设备都可以作为负载，从这个角度讲，拿掉电机剩下的部分是个电源，这就是开源电源技术侧重的内容。

电力电子技术没有放在这里，个人认为这已经是电子学进阶了，包括电机控制也是，电机控制技术和电力电子技术相辅相成，共同发展。我做电机控制更多一点，开关电源我只懂一点点原理，这里也附上我学习电子电子和电机控制的笔记：[电力电子与电机控制](https://xu.yumeng.website/motor-control/)。

电力电子技术可以和开关电源技术电机控制技术联系很紧密。模拟电路数字电路处理信号，电力电子和开关电源在处理功率。实际上模拟电路里已经有了电源的东西了（线性电源），这里是开关电源，很有意思。这两个电源都不可避免的要用负反馈的方式来提高性能，也就是说自动控制原理是也是前置内容，尤其在开关电源设计里面，经典控制理论运用的出神入化。这里也附上我的自动控制原理笔记：[应用数学：控制理论](https://xu.yumeng.website/math/part4/)。


## 参考资料

- [The Art of Electronics - Paul Horowitz, Winfield Hill](https://sg1lib.org/book/2621378/9bb6fa)
- [电路: 修订第5版 - 邱关源](https://sg1lib.org/book/11426662/ceb7fd)
- [模拟电子技术基础 第5版 - 清华大学电子学教研组编；童诗白，华成英原主编](https://sg1lib.org/book/16599034/bb8c3f)
- [数字电子技术基础 - 闫石](https://sg1lib.org/book/14037968/797f47)

