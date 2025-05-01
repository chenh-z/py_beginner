## Q0

#### Class Attribute and Instance Attribute?

Example class :

```python
class ublab_student:
    # Class Attribute
    professor = "Shimonishi""
    def __init__(self):
        # Instance Attribute
        self.grade = "M2"
```

In this example, we can see 2 attribute: `professor`and `grade`.



`professor` is a **class attribute**, obviously all of the professor of `ublab_student` is the same person (in OU ist, one lab has only 1 professor and 1 assosicate professor). And if one student has been changed the professor and staill affilates in ublab, all of the students' professor will be changed. It's like:

```python
>>> C = ublab_student()
>>> C.professor
'Shimonishi'
>>> G = ublab_student()
>>> G.professor
'Shimonishi'
>>> ublab_student.professor = "Ohshita"
>>> C.professor
'Ohshita'
>>> G.professor
'Ohshita'

```



Now, assuming Prof. Shimonishi retired this year, our associate professor Prof.Ohshita became the professor of this lab, all of the students' will be changes **with the change of the class attribute**



I think is easier to understand **instance attribute** `grade`.



For example, to be easier, I create the class with my information, an M2 student `C` in this lab. But this year, senior student `G` got his/her master degree and start the life of "D1"(Doctor 1st year). How to correct it?

```python
>>> G.grade = "D1"
>>> C.grade
'M2'
>>> G.grade
'D1'
```

The **instance attribute** has been change in G and not effected C's grade.


