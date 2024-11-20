#### 2.3.2



Sequence unpacking: bind 2 or more element to one name in for-loop 



For Example:



```python
un_packing = [[10,30],[20,20]]
cnt = 0
for x,y in un_packing:
    if x == y :
    cnt += 1
```



if name in for_loop not be used, replace it by _



e.g.



```python
for _ in range(3)    #0,1,2
    print('1')


Result:
1
1
1
```


