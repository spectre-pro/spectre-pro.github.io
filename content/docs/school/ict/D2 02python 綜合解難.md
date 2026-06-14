---
title: "D2 python 綜合解難"
weight: 10
---

## 建立列表

- 只需直接賦值便可建立列表。
- **建立列表的例子：**
  ```python
  list1 = ["David", "Lily", "Ben"]
  ## 索引對應：list1[0]="David", list1[1]="Lily", list1[2]="Ben"

  list2 = [34, 23, 90, 56, 100]
  ## 索引對應：list2[0]=34, list2[1]=23, list2[2]=90, list2[3]=56, list2[4]=100

  ```
- **初始化的例子：**  
  建立一個擁有 10 個項目的列表，並將所有項目賦值為「0」。  
   ```python  
   list3 = [0] \* 10  
   ## 建立一個包含 10 個 0 的列表，索引由 list3[0] 至 list3[9]
    ```

## 更新列表中的項目

- 列表的索引是由 **0** 開始。
- 建立列表後，才能使用列表名稱加索引來存取指定的項目。
- **將「28」放入列表項目 `list2[0]`：**
  ```python
  list2[0] = 28
  ## list2 的第一個元素由 34 被更新為 28

  ```
- **先讀取列表項目 `list2[2]` 的值，將此值減去 5 後，再將運算結果放入列表項目 `list2[1]`：**
  ```python
  list2[1] = list2[2] - 5
  ## 讀取 list2[2] 的值 (90)，減去 5 得到 85，寫入 list2[1]（原本是 23）

  ```

## 輸出列表

**程式碼：**

```python
list1 = ["David", "Lily", "Ben"]
print(list1[1])
print(list1[0])

```

**輸出結果：**

```text
Lily
David

```

## 複製列表

利用 `for` 循環逐一複製列表項目：

```python
list2 = [34, 23, 90, 56, 100]
new_list = [0] * 5
for i in range(0, 5):
    new_list[i] = list2[i]

```

## 求總和及平均值

以下的程式：

- 將列表的項目逐一相加，計算這位同學完成 **800 米**跑所需時間。
- 將列表的總和除以列表長度，以計算這位同學跑 **100 米**的平均時間。

  ```python
  time = [15.1, 14.9, 15.6, 16.1, 16.8, 17.0, 16.9, 16.5]
  total = 0
  for i in range(0, 8):
      total = total + time[i]
  print(total)      ## Output: 128.9

  avg = total / 8
  print(avg)        ## Output: 16.1125

  ```

## 搜尋數據是否存在於列表中

以下演算法／程式能搜尋數據是否存在於列表中：

```python
target = int(input())
found = False
N = len(the_list)
for i in range(0, N):
    if target == the_list[i]:
        found = True
print(found)

```

## 點算項目

以下演算法／程式用以找出列表中大於輸入值的項目總數：

```python
bound = int(input())
count = 0
N = len(the_list)
for k in range(0, N):
    if the_list[k] > bound:
        count = count + 1
print(count)

```

## 刪除列表中的項目

以下演算法／程式會將列表索引 `P` 的項目刪除。設 `the_list` 是有 `N` 個項目的列表：

```python
N = len(the_list)
for k in range(P, N - 1):
    the_list[k] = the_list[k + 1]

```

> **運作原理簡述：** 從索引 `P` 開始，將後一個項目的值向前覆蓋（例如：`the_list[P] = the_list[P+1]`），直到將最後一個項目向前移。

## 將項目加入列表

以下演算法／程式將新項目 `new_data` 加入列表索引 `P` 的位置，設加入項目後 `the_list` 是有 `N` 個項目的列表：

```python
the_list = the_list + [0]
N = len(the_list)
for k in range(N - 1, P, -1):
    the_list[k] = the_list[k - 1]
the_list[P] = new_data

```

> **運作原理簡述：** 先在列表末端擴充一個位置，然後從最後一個位置開始，將元素逐個向後搬移一位，直到騰出索引 `P` 的空間，最後將 `new_data` 寫入 `the_list[P]`。

## 找出最大或最小的值

以下演算法／程式能找出列表中最大的值：

```python
largest = the_list[0]
N = len(the_list)
for i in range(1, N):
    if the_list[i] > largest:
        largest = the_list[i]
print(largest)

```

## 檢查列表中的值是否按次序排列

以下演算法／程式會檢查列表中的值是否由小至大順序排列：

```python
sorted_list = True
N = len(the_list)
for k in range(0, N - 1):
    if the_list[k] > the_list[k + 1]:
        sorted_list = False
print(sorted_list)

```

## 調動列表中的項目

以下演算法／程式將原本位於索引 `P` 的項目調到列表的第一位。原本排在 `P` 位置前的項目會往後順延。設 `the_list` 是有 `N` 個項目的列表：

```python
temp = the_list[P]
for k in range(P, 0, -1):
    the_list[k] = the_list[k - 1]
the_list[0] = temp

```

> **運作原理簡述：** 先用 `temp` 把索引 `P` 的值存起來，接著把從索引 `0` 到 `P-1` 的項目全部往後移一個位置，最後把 `temp` 放到 `the_list[0]`。

## 找出字符串的長度

- **方法一**：使用內建函數 `len()`

**程式碼：**

```python
word = "Work Hard"
print(len(word))

```

**輸出結果：**

```text
9

```

- **方法二：透過 `for` 循環來計算**

```python
word = "Work Hard"
count = 0
for item in word:
    count = count + 1
print(count)

```

## 找出字符是否存在於字串中

### 運用 `for` 循環找出字符

運用 `for` 循環逐一檢查字符，若目標字符存在於字串中，以下程式會輸出 `True` ；反之，便會輸出 `False`。

**程式碼：**

```python
the_string = "Work Hard!"
target = "a"
found = False
N = len(the_string)

for i in range(0, N):
    if target == the_string[i]:
        found = True

print(found)

```

**輸出結果：**

```text
True

```

### 運用 `while` 循環找出字符

若要找出第一個儲存目標字符的列表索引，可以運用 `while` 循環，當程式找到第一個與目標字符相同的字符時，循環便會停止。

**程式碼：**

```python
the_string = "Work Hard!"
target = "r"
index = -1
found = False
i = 0
N = len(the_string)

while i < N and found == False:
    if target == the_string[i]:
        index = i
        found = True
    i = i + 1

print(index)

```

**輸出結果：**

```text
2

```

## 從字串中提取所需的字符

**程式碼：**

```python
word = "Work Hard!"
sub_word = ""

for i in range(0, 4):
    sub_word = sub_word + word[i]

print(word)
print(sub_word)

```

**輸出結果：**

```text
Work Hard!
Work

```

## 判斷字符的類別

我們可以利用字符的 **ASCII** 來比較字符的大小。

- **大寫字母：** `inputLetter >= "A" and inputLetter <= "Z"`  
  （ASCII 範圍：A=65, B=66, C=67 ... Z=90）
- **小寫字母：** `inputLetter >= "a" and inputLetter <= "z"`  
  （ASCII 範圍：a=97, b=98, c=99 ... z=122）
- **數字：** `inputLetter >= "0" and inputLetter <= "9"`  
  （ASCII 範圍：0=48, 1=49, 2=50 ... 9=57）

## 常見錯誤

### 存取列表中的項目

不存在於列表中的項目是不能被存取的。

- **❌ 錯誤示範：**

```python
list2 = [0] * 5
list2[5] = 5  ## 錯誤！列表長度為 5，最大索引只有 4，會造成 Index Out of Range。

```

- **✔️ 正確示範：**

```python
list2 = [0] * 6
list2[5] = 5  ## 正確！列表長度為 6，最大索引包含 5。

```
