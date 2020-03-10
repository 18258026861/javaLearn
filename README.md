# 多态性

## 对象的多态性

可以直接应用在抽象类和接口上

#### 若编译时（Person p）类型和运行时类型（new Person\(\)）不一样，就会出现多态

这里就会引出动态绑定

```text
Person p = new Student();
p.studentname;  //studentname是Student的变量，实在编译时生成的，那么父类无法调用
p.studentWay();  //studentWay是Studeny的方法，实在运行时生成的，那么便可以使用
                 //当然，如果方法中有子类的变量，那么就会报错。
```

这个时候子类可以看成特殊的父类，那么父类便可引用子类的对象。

### 此时有一个注意点：父类引用子类的这个方法必须建立在重写之前，若在子类中已经重写了这个方法，那调用子类的重写方法。





## 重载：

一个类可以有多个同名方法

**函数重载的好处就是可以给予不同的初始条件（参数）， 来处理相同的事情**

## 重写：

子类可以重写父类的方法

**1.一方面是提供了如何写代码的约定，函数不重写是会报错的, 提高了安全性，**

**2.一方面是多态，当然面向对象的最大好处就是对大型代码分类整理，这点必须要有抽象类，接口类，重载，重写等条件来约束**

