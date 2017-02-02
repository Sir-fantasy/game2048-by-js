# game2048-by-js

通过原生JavaScript 实现的2048.

## 游戏规则：
使用键盘“上、下、左、右”控制方块移动，其他规则请百度“2048”。

## 主要思路：
1.使用一个数组存储4X4个游戏块对象，每个游戏块对象具有数字与类名的属性，通过不同的类名再由CSS展现不同的效果。由游戏棋盘控制滑块移动。
***
2.当按下某方向键时，会判断按键方向并执行相应的方法。   
***
3.按键方法具体如下：若是left，将每行有数字的提取出来，创建一个新数组，在判断新数组相邻两项是否相等。相等则把左边的项数字乘2，右边数字清零。数组全部计算计算完后，在执行一次提取数字的方法，将有数字的项组合成新数组，其余缺少的项全部用新的块对象填充。
***
4.在按键方法中，需要判断是否移动，若移动了则增加数字“2”块，反之则不增加，具体步骤：在执行移动前将数字组合成一个字符串。执行移动后再合成一个字符串，判断两字符串是否相等。相等则未移动，不执行加“2”，不相等则说明移动，执行加“2”。
