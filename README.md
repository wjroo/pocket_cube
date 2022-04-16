# 中文

这是大一学习C语言课程后，突然想用C语言写一个解二阶魔方最短路径还原的程序，于是利用前前后后几个月的闲暇时间，终于实现了这一功能。除了计时部分参考了一下网上代码以外，其它部分都是自己慢慢思索完成。

## 程序简介

程序主要通过角块状态设定、预先计算状态数组及二分查找的方式，最终实现了在1秒内暴力计算输出二阶魔方所有（程序设置为最多输出700条路径）最短还原路径的功能。

补充说明：代码文件编码为gbk，代码变量名命名比较随意。

## 使用方法

确认二阶魔方为6种颜色相对：

- 红对橙
- 黄对白
- 蓝对绿

首先，根据需要输入数字选项，选择复原类型：

1. 标准复原（复原到每一面为同一种颜色的标准状态）
2. 指定复原（指定复原的目标状态）

然后，将一个角块位置（左后下）对好（固定不动）：左=橙，后=绿，下=白。根据提示依次输入剩余7个角块位置的角块信息和颜色朝向，用空格分隔。

最后程序输出所有最短路径信息。数字1~6代表6种旋转方式（一步旋转90度）：

1. 右，顺时针旋转
2. 右，逆时针旋转
3. 上，顺时针旋转
4. 上，逆时针旋转
5. 前，顺时针旋转
6. 前，逆时针旋转

# English (Translated by machine)

After studying C in my freshman year, I suddenly wanted to write a program in C to solve the shortest path to restore the second-order Rubik's cube, so I used my free time for a few months before and after to implement this function. Except for the timing part, which is based on online code, all other parts are done by myself.

## Program Introduction

The program is mainly through the corner block state setting, pre-calculated state array and dichotomous find way, and finally achieved the function of violently calculating the output of all the second-order Rubik's cube within 1 second (the program is set to output a maximum of 700 paths) the shortest restore path.

Additional note: The code file encoding is gbk, the code variable name is more arbitrary.

## Usage

Confirm the second order Rubik's cube as 6 colors relative to each other.

- Red to Orange
- Yellow to white
- Blue against green

First, enter the number options as needed to select the recovery type.

1. Standard recovery (recover to the standard state where each side is the same color)
2. Specify recovery (specify the target state for recovery)

Then, a corner block position (left, back and bottom) to the right (fixed): left = orange, back = green, bottom = white. Follow the prompts to enter the corner block information and color orientation of the remaining 7 corner block positions in turn, separated by spaces.

Finally the program outputs all the shortest path information. The numbers 1~6 represent 6 rotations (90 degree rotation in one step).

1. right, clockwise rotation
2. right, counterclockwise rotation
3. up, clockwise rotation
4. up, counterclockwise rotation
5. front, clockwise rotation
6. front, counterclockwise rotation

# 举例-Example

Input:

```
1
2 2
1 1
0 2
6 1
4 2
5 2
3 1
```

Output:

```
                        耗时1秒.

    1.    1 1 3 5 5       3 6 3 6 3       6 2 4 4
    2.    1 1 3 6 6       3 6 3 6 3       6 2 4 4
    3.    1 1 4 1 1       4 1 6 3 2       3 1 4 4
    4.    1 1 4 2 2       4 1 6 3 2       3 1 4 4
    5.    1 3 1 3 5       3 6 1 4 1       6 3 2 6
          ……
```

## 其它简略运行记录-Other abbreviated run records

```
0 1
1 1
2 1
3 1
4 1
5 1
6 1
	1 3 1 3 1       4 2 4 2 4	……240

0 1
1 1
2 1
6 1
4 2
5 2
3 1
	5 3 6 3 5       3 6 1 4 2       5	……2

0 1
1 1
2 1
3 1
5 0
6 0
4 1
	1 3 2 4 1       3 3 5 1 6       3 2	……67

2 2
1 1
0 2
3 1
4 1
5 1
6 1
	1 1 3 5 4       1 1 3 2 3       5 4 4	……584

2 2
1 1
0 2
6 1
4 2
5 2
3 1
	1 1 3 5 5       3 6 3 6 3       6 2 4 4	……590
```

