# WebMediaAPI

[Web Audio API - 接口参考 | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/API/Web_Audio_API)

## 音频（Audio）的基础知识

### 声音是如何产生的？

**声音是由物体振动产生的**，通过空气、固体、液体等介质进行传输的一种声波，可以被人耳识别的声波的范围是 20Hz~20000Hz 之间，也叫做**可听声波**，这种声波称之为**声音**。

根据声波频率的不同可以主要分为（频率的单位是：[赫兹](https://zhidao.baidu.com/search?word=赫兹&fr=iknow_pc_qb_highlight)）：

- 可听声波：20Hz~20kHz 即20赫兹 到 20000赫兹 之间
- 超声波：> 20kHz
- 次声波：< 20Hz

此外，**人的发声范围一般是 85Hz~1100Hz**。



**赫兹**（Hz），是[国际单位制](https://baike.baidu.com/item/国际单位制/1189599?fromModule=lemma_inlink)中[频率](https://baike.baidu.com/item/频率/19505?fromModule=lemma_inlink)的单位，它是每秒钟的周期性变动重复次数的计量。 

赫兹简称 **赫**。每秒钟[振动](https://baike.baidu.com/item/振动/5801166?fromModule=lemma_inlink)（或[振荡](https://baike.baidu.com/item/振荡/838683?fromModule=lemma_inlink)、[波动](https://baike.baidu.com/item/波动/4741381?fromModule=lemma_inlink)）一次为1赫兹，或可写成次/秒，周/秒。因德国科学家赫兹而命名。



### **声音的三要素**
声音的三要素分别是音调、音量、音色，具体如下：

- **音调：**指的是声音**频率**的高低，表示人的听觉分辨一个声音的调子高低的程度，物体振动的快，发出的声音的音调就高，振动的慢，发出的音调就低。

- **音量：**又称音强、响度，指声音的**振幅**大小，表示人耳对所听到的声音大小强弱的主观感受。

- **音色：**又称音品，指不同声音表现在波形方面总是有与众不同的特性，不同的物体振动都有不同的特点，反映每个物体发出的声音的特有的品质，音色具体由**谐波**决定，好听的声音绝不仅仅是一个正弦波，而是谐波。

    

### 电磁波

> 从科学的角度来说，电磁波是能量的一种，凡是高于绝对零度的物体，都会释出电磁波。且温度越高，放出的电磁波波长就越短。**电磁波的传播速度相当于光速**，正像人们一直生活在空气中而眼睛却看不见空气一样，除光波外，人们也看不见无处不在的电磁波。



### 音频采样率（）

音频采样率是指录音设备在单位时间内对模拟信号采样的多少 ，

**简单来说采样率是多少 就是 每秒对声音采集多少次** ，

采样频率越高，[机械波](https://upimg.baike.so.com/doc/6012758-6225745.html)的波形就越真实越自然。在当今的主流采集卡上，采样频率一般共分为11025Hz、22050Hz、24000Hz、44100Hz、48000Hz五个等级，11025Hz能达到AM调幅广播的声音品质，而22050Hz和24000HZ能达到FM调频广播的声音品质，44100Hz则是理论上的CD音质界限，48000Hz则更加精确一些。



### 声音的振幅 与 频率有什么关系？

振幅和频率是从两个不同的概念来描述波动的.他们之间没有明显了联系.


**振幅**决定**能量的大小**,

**频率**决定**声调的高低**，

可简单理解成我们听到的声响一样.调好的吉他,弹同一根琴弦,弦振动的频率是一样的.但弹的力度不同,我们听到的声响是不同的.也就是波动的振幅不同造成的.



### 振动加速度、振幅、频率三者关系

> 在低频范围内，振动强度与位移成正比；在中频范围内，振动强度与速度成正比；在高频范围内，振动强度与加速度成正比。

因为频率低意味着振动体在单位时间内振动的次数少、过程时间长，速度、加速度的数值相对较小且变化量更小，因此振动位移能够更清晰地反映出振动强度的大小；而频率高，意味着振动次数多、过程短，速度、尤其是加速度的数值及变化量大，因此振动强度与振动加速度成正比。

也可以认为，振动位移具体地反映了间隙的大小，振动速度反映了能量的大小，振动加速度反映了冲击力的大小。

振动加速度的量值是单峰值，单位是重力加速度[g]或米/秒平方[m/s2]，1[g] = 9.81[m/s2]。

最大加速度20g（单位为g）。

最大加速度=0.002×f2（频率Hz的平方）×D（振幅p-pmm）  f2：频率的平方值。



举例：10Hz最大加速度=0.002×10*10×5=1g

在任何頻率下最加速度不可大于20g

最大振幅5mm



## **MP3**

MP3的全称应为MPEG1 Layer-3音频文件，[MPEG](https://upimg.baike.so.com/doc/2905760-3066372.html)(Moving Picture Experts Group)在汉语中译为活动图像专家组，特指活动影音压缩标准，MPEG音频文件是MPEG1标准中的声音部分，也叫MPEG音频层，它根据[压缩质量](https://upimg.baike.so.com/doc/25397656-26420788.html)和编码复杂程度划分为三层，即Layer-1、Layer2、Layer3，且分别对应[MP1](https://upimg.baike.so.com/doc/926478-979306.html)、MP2、MP3这三种声音文件，并根据不同的用途，使用不同层次的编码。

MPEG[音频编码](https://upimg.baike.so.com/doc/940309-993829.html)的层次越高，编码器越复杂，[压缩率](https://upimg.baike.so.com/doc/6899857-7120518.html)也越高，MP1和MP2的压缩率分别为4:1和6:1-8:1，而MP3的压缩率则高达 10:1-12:1，也就是说，一分钟[CD音质](https://upimg.baike.so.com/doc/6744652-6959195.html)的音乐，未经压缩需要10MB的存储空间，而经过MP3压缩编码后只有1MB左右。

不过MP3对音频信号采用的是[有损压缩](https://upimg.baike.so.com/doc/5959165-6172112.html)方式，为了降低声音[失真度](https://upimg.baike.so.com/doc/6150514-6363708.html)，MP3采取了"感官编码技术"，即编码时先对音频文件进行频谱分析，然后用过滤器滤掉噪音电平，接着通过量化的方式将剩下的每一位打散排列，最后形成具有较高压缩比的MP3文件，并使压缩后的文件在回放时能够达到比较接近原音源的声音效果。

(另[MP3PRO](https://upimg.baike.so.com/doc/7901282-8175377.html): mp3PRO编码器将音频的录音分成两个部分:mp3部分和PRO部分。mp3部分分析低频段(Low Frequency Band)信息，并将其编码成通常的mp3文件数据流。这就使得编码器能够集中编码更少的有用信息，获得更佳品质的编码效果。

同时，这也保证了 mp3PRO文件同老的mp3播放器的兼容性。PRO部分分析的则是高频段(High Frequency Band)信息，并将其编码成mp3数据流的一部分，而这些通常在老的mp3[解码器](https://upimg.baike.so.com/doc/170972-180621.html)里是被忽略的。新的[mp3PRO](https://upimg.baike.so.com/doc/7901282-8175377.html)解码器会有效地利用这部分数据流，将两段(高频段和低频段)合并起来产生完全的音频带，达到增强[音质](https://upimg.baike.so.com/doc/3050351-3215577.html)的效果。

