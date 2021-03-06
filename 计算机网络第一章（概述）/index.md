## 计算机网络概述

1.  计算机网络定义： 一个计算机网络是由资源子网和通信子网构成的

    - 资源子网： 负责信息处理
    - 通信子网： 负责全网中的信息传递

2.  协议的定义： 是网络通信实体之间在数据交换过程中需要遵循的规则或约定，是计算机网络有序运行的重要保证

    三个基本要素：

    - 语法： 定义实体之间交换信息的格式与结构
    - 语义： 定义实体之间交换的信息中需要发送那些控制信息，这些信息的具体含义，以及针对不同含义的控制信息，接收信息端应如何响应
    - 时序（同步）：定义实体之间交换信息的顺序以及如何匹配或适应彼此的速度

3.  计算机网络的功能

    1. 核心功能是： 实现资源共享
    2. 包括
       - 硬件资源共享： 如云计算、云存储
       - 软件资源共享：如软件即服务（SaaS）
       - 信息资源共享： 如信息交换

4.  拓扑结构分类

    - 星形拓扑结构： 多见于局域网、个域网中
      - 优点：
        1.  易于监控与管理
        2.  故障诊断与隔离容易
      - 缺点： 中央节点是网络的瓶颈，一旦故障，全网瘫痪，网络规模受限于 中央节点的端口数量
    - 总线型拓扑结构: 在早期的局域网中比较多见
    - 环形拓扑结构：多见于早期的局域网、园区网和域域网中
      - 优点：
        1.  所需电缆长度短
        2.  可使用光纤
        3.  避免冲突
        4.  网络性能稳定（闭合回路）
      - 缺点： 故障检测麻烦（任意节点出现故障都会造成网络瘫痪）
    - 网状拓扑结构：多见于广域网、核心网络
    - 树形拓扑结构： 目前很多局域网采用这种拓扑结构
    - 混合拓扑结构： 绝大多数实际网络的拓扑都属于混合拓扑，比如 internet

5.  计算机网络结构：
    1. 网络边缘
    2. 接入网络
    3. 网络核心
    
    > 比较典型的分组交换设备是路由器和交换机等
    
6.  数据交换技术：
    1.  电路交换： 最早出现的一种交换方式
    2.  报文交换： 现在计算机网络没有采用，不适用于实时通信，不得不丢弃报文
    3.  分组交换： 目前计算机网络广泛采用的技术
        - 优点：
          - 交换设备存储容量要求低
          - 交换速度快
          - 可靠传输效率高
          - 更加公平
7.  时延： 通常将连接两个结点的直接链路称为 一个 ‘跳步’，简称跳

    - 传输时延： 当一个分组在输出链路发送时，从发送第一位开始，到发送完最后一位为止，所用的时间，称为传输时延，也称为发送时延，记为 dt。设分组长度 Lbit, 链路宽度（即速率）Rbit/s, 则 dt=L/R
    - 传播时延： 信号从发送端发送出来，经过一定距离的物理链路到达接收端所需的时间，称为传播时延。设物理链路长度 Dm, 信号传播速度 Vm/s, 则 dp=D/V.
    - 时延带宽积： 一段物理链路的传播时延 dp 与链路宽度 R 的乘积，记为 G, G=dp\*R, G 的单位是（bit). 物理意义在于：如果将物理链路看作一个传输数据的管道的话，时延带宽积表示一段链路可以容纳的数据位数，也称为以位为单位的链路长度

8.  吞吐量： 对于分组交换网络，源主机到目的主机的吞吐量在理想情况下约等于瓶颈链路的带宽，即等于链路的带宽中的最小值
9.  计算机网络体系结构的含义： 计算机网络所划分的层次以及各层协议的集合
10. OSI 参考模型: 将整个计算机网络的通信功能分为 7 层，由低层至高层分别是：
    - 物理层
    - 数据链路层
    - 网络层
    - 传输层
    - 会话层
    - 表示层
    - 应用层
11. TCP/IP 参考模型： 由低层至高层分别是：
    - 网络接口层、网络互联层（IP协议-核心）
    - 传输层（TCP协议与UDP协议）
    - 应用层
12. 3种参考模型和OSI参考模型有关术语： 各层对应的PDU名称：
    - 应用层： 报文
    - 传输层： 段（数据段或报文段）
    - 网络层： 分组或包
    - 数据链路层： 帧
    - 物理层： 位流或比特流
13. 计算机网络与因特网发展简史： ARPAnet 是第一个分组交换计算机网络，也是当今因特网的祖先