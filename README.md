# ����

���Ǵ�һѧϰC���Կγ̺�ͻȻ����C����дһ�������ħ�����·����ԭ�ĳ�����������ǰǰ��󼸸��µ���Ͼʱ�䣬����ʵ������һ���ܡ����˼�ʱ���ֲο���һ�����ϴ������⣬�������ֶ����Լ�����˼����ɡ�

## ������

������Ҫͨ���ǿ�״̬�趨��Ԥ�ȼ���״̬���鼰���ֲ��ҵķ�ʽ������ʵ������1���ڱ��������������ħ�����У���������Ϊ������700��·������̻�ԭ·���Ĺ��ܡ�

����˵���������ļ�����Ϊgbk����������������Ƚ����⡣

## ʹ�÷���

ȷ�϶���ħ��Ϊ6����ɫ��ԣ�

- ��Գ�
- �ƶ԰�
- ������

���ȣ�������Ҫ��������ѡ�ѡ��ԭ���ͣ�

1. ��׼��ԭ����ԭ��ÿһ��Ϊͬһ����ɫ�ı�׼״̬��
2. ָ����ԭ��ָ����ԭ��Ŀ��״̬��

Ȼ�󣬽�һ���ǿ�λ�ã�����£��Ժã��̶�����������=�ȣ���=�̣���=�ס�������ʾ��������ʣ��7���ǿ�λ�õĽǿ���Ϣ����ɫ�����ÿո�ָ���

����������������·����Ϣ������1~6����6����ת��ʽ��һ����ת90�ȣ���

1. �ң�˳ʱ����ת
2. �ң���ʱ����ת
3. �ϣ�˳ʱ����ת
4. �ϣ���ʱ����ת
5. ǰ��˳ʱ����ת
6. ǰ����ʱ����ת

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

# ����-Example

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
                        ��ʱ1��.

    1.    1 1 3 5 5       3 6 3 6 3       6 2 4 4
    2.    1 1 3 6 6       3 6 3 6 3       6 2 4 4
    3.    1 1 4 1 1       4 1 6 3 2       3 1 4 4
    4.    1 1 4 2 2       4 1 6 3 2       3 1 4 4
    5.    1 3 1 3 5       3 6 1 4 1       6 3 2 6
          ����
```

## �����������м�¼-Other abbreviated run records

```
0 1
1 1
2 1
3 1
4 1
5 1
6 1
	1 3 1 3 1       4 2 4 2 4	����240

0 1
1 1
2 1
6 1
4 2
5 2
3 1
	5 3 6 3 5       3 6 1 4 2       5	����2

0 1
1 1
2 1
3 1
5 0
6 0
4 1
	1 3 2 4 1       3 3 5 1 6       3 2	����67

2 2
1 1
0 2
3 1
4 1
5 1
6 1
	1 1 3 5 4       1 1 3 2 3       5 4 4	����584

2 2
1 1
0 2
6 1
4 2
5 2
3 1
	1 1 3 5 5       3 6 3 6 3       6 2 4 4	����590
```

