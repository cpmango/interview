# 

## 什么是鸭子类型

** "当看到一只鸟走起来像鸭子、游泳起来像鸭子、叫起来也像鸭子，那么这只鸟就可以被称为鸭子" **

- 关注点在对象的行为，而不是类型（duck typing）
- 比如 file，StringIO，socket 对象都支持read／write方法（file like object)
- 再比如定义了＿iter＿魔术方法的对象可以用for迭代

```python
class Duck:
  def quack(self):
    print("gua gua")


class Person:
  def quack(self):
    print(＂我是人类，但我也会 gua gua gua＂)


def in_the_forest(duck):
  duck.quack()


def game():
  donald=Duck()
  john=Person()
  in_the_forest(donald)
  in_the_forest(john)


game()
```

![Screenshot](img/2023-03-30_02-30.jpg)
