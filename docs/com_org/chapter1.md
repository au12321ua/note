## 一些缩写解释

1. `ISA`: instruction set architecture 指令集架构
2. `CPI`: cycles per instruction 每个指令所花费的周期数（一般使用平均CPI）

## CPU性能相关计算公式

1. $\text{CPU time} = \frac{\text{CPU clock cycles}}{\text{CPU rate}} = \text{CPU cycles} \times \text{CPU cycle time}$

    简单来说就是“总时间=周期数/频率=周期数×每个周期花费的时间”

2. $\text{clock cycles} = \text{instruction count} \times \text{CPI}$

    简单来书就是“周期数=指令数×每个指令平均花费的周期”

3. $\text{CPU time} = \frac{\text{Instructions}}{\text{program}} \times \frac{\text{clock cycles}}{\text{Insturction}} \times \frac{\text{Seconds}}{\text{clock cycles}}$

    这里就是前两个公式的汇总，第一个分式算出了平均每个程序的指令数，第二个算出了CPI，第三个算出了每个时钟周期消耗的时间