# Lesson 10 , 11  (oop  (object oriented programming) )



1. function in oop -----> named (method) ------> Action

2. property in oop ----> named  attribute 

3. python everything is object 

   

4. Types Object Oriented Programming 

    

   1. Inheritance
   2. Polymorphism
   3. Encapsulation
   4. Abstraction

   

     

      ![Object-Oriented-Programm-Python-1](C:\Users\DELL\Downloads\Object-Oriented-Programm-Python-1.jpg)

   

   

   Notes for  Object Oriented Programming in python

   

   <img src="C:\Users\DELL\OneDrive\Pictures\programming\Screenshots\260297082_1283582472068507_5322580700666199367_n.jpg" alt="260297082_1283582472068507_5322580700666199367_n" style="zoom:50%;" />

   

   <img src="C:\Users\DELL\OneDrive\Pictures\programming\Screenshots\260465141_1283582485401839_5315521265344351752_n.jpg" alt="260465141_1283582485401839_5315521265344351752_n" style="zoom:50%;" />

   <img src="C:\Users\DELL\OneDrive\Pictures\programming\Screenshots\260467214_1283582498735171_8783822189578544862_n.jpg" alt="260467214_1283582498735171_8783822189578544862_n" style="zoom:50%;" />

   <img src="C:\Users\DELL\OneDrive\Pictures\programming\Screenshots\260318222_1283582595401828_8964489703369501461_n.jpg" alt="260318222_1283582595401828_8964489703369501461_n" style="zoom:50%;" />

<img src="C:\Users\DELL\OneDrive\Pictures\programming\Screenshots\289393277_178032474619203_1205241032432669114_n.jpg" alt="289393277_178032474619203_1205241032432669114_n" style="zoom: 50%;" />





1.  ### Encapsulation 

   

```python
# name Class
class Calc:
    # Encapsulation مع كتابه كلمه self انت كدا استخدمت مبدا   
    # Method 1 named sum
    def sum (self,x,y):
        return x+y
    # Method 2 named mult
    def mult (self,x,y):
        return x*y
    # Method 3 named div
    def div (self,x,y):
        return x/y
    # Method 4 named power
    def power (self,x,y):
        return x**y
  # calling the class in varible oper  
oper = Calc()
# print(object in class Calc using method div)
print(oper.div(40,5))    


```

2. ### inheritance  

   -  لازم تاخد بالك منها  coding فيه مفاهيم في ال 

   ​            DRY  (don't repeat your self)

```python

class Calc:
    def summ (self,x,y):
        return x+y
    def mult (self,x,y):
        return x*y

class SicCalc(Calc):
    def div (self,x,y):
        return x/y
    def power (self,x,y):
        return x**y
    # error ف هيطلع ليا method تانيه Class كدا انا اخذت من       
    # Class Calc  ف المفروض اخد وراثه من 
oper = SicCalc()    
print(oper.summ(3,4))
print(oper.mult(3,4))
print(oper.div(3,4))
print(oper.power(3,4))
```

this is the contractor   

```python
def __init__(self,name):
    print(f"Welcome {name}")
  
```

​    -  inheritance (multiple intelligences)

```python

class A:

     def do(self):
        print("in A")
        
class B(A):
   pass
        
class C:
     def do(self):
        print("in V")

# كدا ال (دي) وارثه من ال  (بي و ال سي) ف ال دي ترح لل بي تشوف هي وارثه من اي و بعدها تطبع او تنفذ اللي مطبوع

class D(B,C):
    pass

        
object_1 = D()
object_1.do()
# (MRO)Method Resolution Order
# الداله دي بتعرفني اي الميسود او الداله اللي هتشتغل الاول
print(D.mro())    
```



3. ###   Polymorphism

   #####     هو / انا عندي 2 كلاس او اكثر  فيهم 2 ميسود (دالتين) او اكثر , بنفس الاسم و بتأدي نفس الغرض لاكن مينفعش اورثهم  , !! ليه   عشان اللوجيك بتاعهم مختلف او العمليات بتاعت الدوال                     مختلفه رغم ان هي نفس الاسم           

```python
# كان ممكن اورثها بس مينفعش هنا, ليه , عشان كل داله بتطبع ناتج مختلف  do هو زي المثال اللي فوقه , زي داله

# , class User , class Investor مثال تاني  , عندنا شركه او مصنع  هنعمل 
#  polymorphismو هتكون الهمليات مختلفه ف بالتالي هنستخدم ال  salary ف هيكون فيهم كلهم داله باسم  class Manager 



```







 

-  و للي اخذناه oop  مثال بسيط علي ال 
