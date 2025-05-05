## Q0

#### 类属性和实例属性?

作为举例，请看下面的类 : 

```python
class ublab_student:
    # Class Attribute
    professor = "S"
    def __init__(self):
        # Instance Attribute
        self.grade = "M2"
```

在这个例子中，我们可以看到两种属性：`professor`和 `grade`.

`professor` 是一个 **类属性**, 显然所 `ublab_student` 中学生的指导教授是同一位is the same person (至少在OUist，一个实验室只有一位教授和副教授). 并且指导教授改变时，所有学生的指导教授都会随之改变。例如：

```python
>>> C = ublab_student()
>>> C.professor
'S'
>>> G = ublab_student()
>>> G.professor
'S'
>>> ublab_student.professor = "O"
>>> C.professor
'O'
>>> G.professor
'O'
```

现在，我们假设S教授今年退休，我们的副教授O教授成为了这个实验室的指导教授，于是所有学生的指导教授将 **随着类属性改变**

我认为 **实例属性** `grade`将更容易理解

在这里例子中，为了方便，我创建类时使用了我的个人信息 —— 实验室中一位修士2年生，C。但今年，我的前辈G获得了ta的修士学位并且开始了博士生活。那么该如何修改？

```python
>>> G.grade = "D1"
>>> C.grade
'M2'
>>> G.grade
'D1'
```

这样， G中**实例属性** 被更改，并且没有影响到C的实例属性Grade
