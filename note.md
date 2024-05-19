學習到教程4 12:05

## 資料類型
Python 的內建型態主要分為以下三種：

數值型態：int, float, bool
字串型態：str, chr
容器型態：list, dict, tuple

#### 複製串列 
「串列[:]」，效果等同於複製完整的串列，如果使用「b=a」的做法，雖然看起來像是複製了，但實際上 a 和 b 指向了同一個串列，所以當 a 刪除了一個項目時，b 也會跟著改變，然而如果使用「d=c[:]」的做法，會建立一個「全新」的串列，當 c 發生改變時，不會影響 d。
```
c = [1, 2, 3]
d = c[:]     # 複製 c 的所有項目變成一個新串列
del(c[1])    # 刪除 c 的第二個項目
print(c)     # [1, 3]
print(d)     # [1, 2, 3]
```

#### *name 代表可以接受任意數量的參數
```
def report(name, *grades): 
    total_grade = 0
    for grade in grades:
        total_grade += grade
    print(f"{name}'s totol grade is {total_grade} ")

report ('Avery',60, 99, 40, 88)
```
