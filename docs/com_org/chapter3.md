## Chapter3_Arithmetic for Computers

### 更快的加法器

#### CLA（Carry-Lookahead Adder）

在RCA中，进位位与和位一起计算，并且每个级必须等到前一个进位位计算完毕后才能开始计算自己的进位位，导致速度较慢。

而在CLA中，提前计算出了前几位的进位，使得后续全加器不必前一位等待门延迟较高的和位计算，从而大大提高了速度。

一般要保持扇入扇出与提前进位的平衡，若扇入扇出很大，也会造成时间的延长。

它的另一个优点是速度稳定，有利于流水线运行。

#### Carry-Skip Adder

Carry-Skip Adder是一种并行加法器，它通过跳过一些不需要进位的位来减少进位传递的时间。

具体来，对于某一位，若进位传递函数（Pi）的所有输入都为1或都为0，则该位的进位可以直接跳过中间位，直接传递到后续的某一位。这样可以减少进位传递的延迟，从而加快加法运算的速度。比如：1与1，可以直接进位1；0与0就直接进位0。

平均来说，可以加快一半的进位速度，但不稳定，不适用于流水线运行。

#### CSA（Carry-select Adder）

进位选择加法器一般由纹波进位加法器和多路复用器组成。使用进位选择加法器将两个 n 位数字相加是通过两个加法器（因此是两个纹波进位加法器）完成的，以便执行两次计算，一次假设进位为零，另一次假设进位为零这将是一个。计算出两个结果后，一旦知道正确的进位输入，就可以使用多路复用器选择正确的总和以及正确的进位输出。

这种设计可以显著提高加法器的运算速度，因为不需要等待逐位的进位传递。但是，它也增加了电路的复杂性和面积，因为需要额外的加法器和多路复用器。

在实际应用中，进位选择加法器适用于需要高速计算的场合，如数字信号处理器（DSP）和图形处理单元（GPU）等。尽管它的硬件成本较高，但在性能要求较高的场景下，这种额外的成本是值得的。

### 乘法计算

乘数n位，被乘数n位，积2n位。

用n次加法实现乘法，开始时乘数储存在积的后n位，被乘数始终与积的前n位对齐。每一次加法，被乘数与“积”的最后一位相乘，再对应的加到积上，最后再将积右移。这个过程进行n次，即得到了最终的结果。

比如：

![示例](img_com/mult1.png)