# 数学 一年级

## 数与代数

- **数字** Number
  - 零 `0` (Zero)
  - 一 `1` (One)
  - 二 `2` (Two)
  - 三 `3` (Three)
  - 四 `4` (Four)
  - 五 `5` (Five)
  - 六 `6` (Six)
  - 七 `7` (Seven)
  - 八 `8` (Eight)
  - 九 `9` (Nine)
  - 十`10` (Ten )
- **比较运算符**
  - 大于 `>` (Greater than)
  - 小于 `<` (Less than)
  - 等于 `=` (Equality)
- **数学运算符**
  - 加 `+` (Addition) 加数 + 加数 = 和
  - 减 `-` (Subtraction) 被减数 - 减数 = 差

## 图形与几何

- 长方体(Cuboid)、立方体(Cube)、圆柱(Cylinder)、球(Sphere)
- 矩形(Rectangle)、正方形(Square)、圆(Circle)
- 三角形(Triangle)、四边形(Trapezium)、五边形(Pentagon)、平行四边形(Parallelogram)

## 统计与概率

## 综合与实践

```py
# 十以内的加减法
import random

def random_num():
    a = random.randint(0,10)
    v = random.choice(["+","-"])
    if v == "-":
        b = random.randint(0,a)
    else:
        b = random.randint(0,10)
    return a,b,v

def main():
    s = 0
    t = 0
    f = 0
    while True:
        s+=1
        a,b,v = random_num()
        i = input(f"{a} {v} {b} = ")
        if i == "":
            print(f"共{(s-1)}题，答对{t}题，正确率：{t/(s-1):.2%}")
            exit()
        try:
            match v:
                case "+":
                    n = a + b
                case "-":
                    n = a - b
            if i == str(n):
                t+=1
            else:
                print(f"错误!应为{n}")
                f+=1
        except:
            f+=1
            print("Error.")

if __name__ == "__main__":
    main()
```
