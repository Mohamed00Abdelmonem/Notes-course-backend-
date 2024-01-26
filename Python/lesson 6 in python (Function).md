# lesson 6 and 7 in python (Function)

- #### modularity (الداله هي اول خطوه في ال مودلارتي  وهو عشان لما بتيجي تقسم الكود لاجزاء صغيره  عشان نقدر نستحدمها عده مرات  and notes componace  هي تقسيم الكود او تفتيته لاجزاء صغيره)

- #### function consist of  

  1. definition 

  2. call

     ```python
     # definition
     
     # x,y هي تسمي argumnts, parameterse
     def function_name(x,y):
         # body
       # return with value  عشان نقدر نخزنها في متغير او في قواعد البيانات او اي شئ
       return x+y
     
     #calling
     print(function_name(3,5))
     ```

  

  

- ####  conventions  (عادات و تقاليد المبرمجين) 

  1. اسم الداله يكون lowercase 









- #### types parameterse or argumnts

  1. required 

     ```python
     def mysum(x,y):
        return x+y
     print(mysum(3))
     # كدا عندي خطأ من نوع ريكوايرد و بيزوشينال عشان عندي قيمه اكس بس 
        
     ```

     

  2. keyword or  positional

     ```python
     def mysum(x,y):
        return x+y
     print(mysum(y=3, x=5))
     # الغرض ان اخصص لكل متغير القيم الخاصه بيه عشان هو بيختار للمتتغير الاول ثم الثاني
     ```

     

  3. default 

     ```python
     def mysum(x=0,y=0):
        return x+y
     #ممكن مابصيش قيم عشان انا مديها قيمه افتراضيه ب صفر
     print(mysum(3,5)
     ```
  
     
  
  4. variable length
  
     ```python
     def mysum(*number):
         # كدا هو هياخد اي عدد من المتغيرات او القيم 
         print(number)
         # كدا هيطبع مجموع كل القيم
         print(sum(number))
     
     mysum(1,3,4,5,6,7,8,9)    
     
     # في فكره تانيه ف ال varible lenth
     
     def mysum(args,*number):
         # كدا هو هياخد اول قيمه هتكون لل ارجس  لا كن باقي القيم هتكون بتاعت ال نامبر
             print(args) # output = 1
             print(number) # output = (3,4,5,6,7,8,9)
         # كدا هيطبع مجموع كل القيم
             print(sum(number) + args)
     
     mysum(1,3,4,5,6,7,8,9)
     ```
  
     - Anonymous  Function (الداله المجهوله)
     
       ```python
       #   definition       calling
       x = lambda(x,y : x+y) (3,5)
       print(x)
       ```
     
       