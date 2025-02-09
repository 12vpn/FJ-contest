# CY的水题比赛

---

额外的编译命令 -Ofast -std=c++11

---
## frog

#### 时间：1s
#### 内存：5MB
鲁克一直对背诵课文很苦恼。每次Soldier Xu让他默写时，他都只记得句子的位置，但是不记得句子内容。
于是他决定让你写个程序帮助他。
Soldier Xu的课文很长，多达19260817个字母。现在她让鲁克默写第n到第m个字符(从0开始编号，包括第n个字符但不包括第m个字符)。
#### 输入
##### 第一行，19260817个字符。
##### 第二行，两个数字，n和m
#### 样例：
输入：
由以下程序运行产生
```cpp
#include<fstream>
std::ofstream fout("frog.in");
int main()
{
	for (int i = 0; i < 19260817;i++)
		fout.put(i % 26 + 'a');
	fout << '\n';
	fout << 26 << ' ' << 28 << '\n';
	return 0;
}
```
##### 输出：
ab

---

# 鲁克的钱。
---
### 文件名：money.cpp
### 输入：money.in
### 输出：money.out
---
鲁克王国的每一枚钱都是鲁克亲手雕刻的。每一枚钱上依次有环形的n个数字，钱可以旋转。
由于鲁克技术高超，没有钱是一样的。但是令他苦恼的是，徐大兵妄图通过造假币取代他的地位。
所幸，徐大兵技术不高明，每次造的一批假币中，必有一样的。
现在给出一批货币，请判断是否有假币。
### 是，请输出
## "All the currency in circulation will be destroyed by Luke."
### 否则，请输出
## "Soldier Xu is sleeping."
---
## 输入：
第一行，一个整数m，表示钱的数量。
第二行，一个整数n，表示每枚钱上数字的数量。
保证n*m<=1e6。
接下来m行，每行n个数，依次代表钱上的各个数字。
## 输出：
共一行，
### "All the currency in circulation will be destroyed by Luke."
或
### "Soldier Dandan is sleeping."
---
## 数据范围：
#### 对于50%的数据，输出
### "All the currency in circulation will be destroyed by Luke."，
即可骗分。
#### 对于另外50%的数据，输出
### "Soldier Dandan is sleeping."，
即可骗分。

---
# 鲁克过河
---
### 时间：1s
### 内存：256MB
### 文件名：river.cpp
---
鲁克要亲自押送他的货物过河。河流自西向东，流速不计。鲁克在目的地的西边1距离单位，南边1距离单位。鲁克在岸上的相对速度为1,在水中的相对速度为v,

$$ 0<v<\sqrt{2}/2 $$
。
## 输入
第一行，一个整数n，代表询问总数。
第二行，一个整数m，代表保留的小数位数。
接下来n行，每行一个浮点数v，代表鲁克在水中的相对速度。
## 输出

共n行，每行一个对应的答案——一个有m位小数的浮点数。不要使用科学计数法。

---

## 样例
### 输入
#### 3
#### 3
#### 0.1472
#### 0.544173
#### 0.20241

### 输出
#### 0.149
#### 0.649
#### 0.207

---

## 数据范围
1.  n=100,  m=1
2.  n=200,  m=2
3.  n=300,  m=3
4.  n=400,  m=4
5.  n=500,  m=5
6.  n=10000,m=1
7.  n=200000,m=2
8.  n=300000,m=8
9.  n=400000,m=9
10. n=500000,m=10

### 提示
这题的三分出题者写了一个晚上精度还是很低，于是决定让你们找规律。
对于每个询问，都可以O(1)求解。公式为某正比例函数除以根号下某二次函数（都是关于v的（废话））。

---
## 鲁克的公司

### 内存：256MB
### 时间：1s
### 文件名：tips.cpp
### 输入：tips.in
### 输出：tips.out
为了更好地享受服务，鲁克决定成立鲁克服务有限公司。该公司员工没有工资，全部收入来源于鲁克的小费。该公司为树形结构，每个节点可能有子公司。每个公司至多有一个母公司。对于每个节点，自己为0级子公司，所有直接子公司称为1级子公司，直接子公司的直接子公司称为2级子公司，以此类推。公司编号为1到n，1号为总公司。

###  输入：
#### 第一行，一个数字n，表示公司总数。
#### 第二到第n行，两个数字a，b，表示b是a的直接子公司。
#### 接下来一行，一个数字m，表示操作总数。
#### 接下来m行，有两种可能的操作。
##### 1 a b c，表示鲁克给a公司的所有b级子公司发c元小费。公司内部的小费分配鲁克不屑于管理。 这种操作不用输出。
##### 2 a，表示鲁克查询a公司获得的小费总和。输出a公司获得的小费总和。

### 1<=n,m<=90000
---
# 完