### 3197.Find-the-Minimum-Area-to-Cover-All-Ones-II

事实上将一个矩阵分成三个互不相交的子矩形，只有如下六种形式：
```
        1.        2.      3.
                    
        ┌－┐      ┌┐┌┐    ┌－┐
        └－┘      └┘└┘    └－┘
        ┌－┐      ┌－┐    ┌┐┌┐
        └－┘      └－┘    └┘└┘
        ┌－┐
        └－┘
        
        4.       5.      6.
        ┌┐┌┐┌┐   ┌ ┐┌┐    ┌┐┌ ┐
        └┘└┘└┘   │ │└┘    └┘│ │
                 │ │┌┐    ┌┐│ │
                 └ ┘└┘    └┘└ ┘
```
对于每种形式，只有两条分割线。我们可以用o(MN)的时间遍历分割线的位置，就可以确定三个子矩阵的边界。对于每一个子矩阵，我们再遍历其中的元素，确定包含所有元素1的最小矩阵即可（同3135）。
                 