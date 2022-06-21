# note on super()

## Example setup

```python
class A:
    def name(self):
        print('A')
class B:
    def name(self):
        print('B')
class C(A,B):
    def name(self):
        print('C')
class D(C):
    def name(self):
        print('D')
        
a = A()
b = B()
c = C()
d = D()
```

## ```_mor_```

**Definition:  ```_mor_```** records the order in which each class is inherited.

**Example: **
```
D.__mro__
```

output: 

```
(__main__.D, __main__.C, __main__.A, __main__.B, object)
```

## super(class, obj)

**Definition: super(class, obj)** returns the superclass of class in obj by ```_mor_```.

**Example: **

```super(C, d).name()``` output: A

**Explaination: **

mor for d is (__main__.D, __main__.C, __main__.A, __main__.B, object), in this the superclass of C is **A** 




