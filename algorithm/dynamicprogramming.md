### dynamic programming
动态规划常常适用于有重叠子问题和最优子结构性质的问题，动态规划方法所耗时间往往远少于朴素解法。动态规划背后的基本思想非常简单。
大致上，若要解一个给定问题，我们需要解其不同部分（即子问题），再根据子问题的解以得出原问题的解。通常许多子问题非常相似，为此动态规划法
试图仅仅解决每个子问题一次，从而减少计算量：一旦某个给定子问题的解已经算出，则将其记忆化存储，以便下次需要同一个子问题解之时直接查表。
这种做法在重复子问题的数目关于输入的规模呈指数增长时特别有用。

#### 步骤
+ 拆分子问题，建立状态转移方程。即寻找规律，得到f(n) = f(n-1) + P，f(n)为结果，P为f(n-1)的结果加上某些条件
+ 缓存结果用以复用，复用结果可以避免无用的重复计划

#### 遍历字串(序列)的方式
a b c d e
+ 以当前结点为开始结点，依次向后遍历以这个结点为开头的所有子序列，|a | ab | abc | abcd | abcde |，再以后一个结点依次遍历(正常思维，用于暴力破解)
+ 以子序列长度的标准，遍历长度为1 2 ... n的子序列
+ 以当前结点为结束结点，依次向后遍历这个结点为结尾的所有子序列，a为结尾只有a，b为结尾有ab和b，c为结尾有abc bc c(产生递归关系，通常用于动态规划)