# Lesson 15 ( python intermediate)



- ### list  comprehension 

   

  ```python
  names = ['Mohamed', 'Ahemd', 'Amr', 'Abdelmonem']
  # list comprehention
  result = [len(n) for n in names if len(n)>3]
  result_2 = [len(n) if len(n)>3 else '_' for n in names] # output = [7, 5, '_' , 10] 
  print(result)
  print(reusult_2)
  ```

  

- generator (بيكون سريع شويه)

  ```python
  names = ['Mohamed', 'Ahemd', 'Amr', 'Abdelmonem']
  #  generator
  result = (len(n) for n in names if len(n)>3)
  print(result)
  
  #  list بيطبع المكان بتاعه في الذاكره او المومري  و عشان يكون ناتج للقراءه بتحوله لل  
  ```

  - ### Functional  Programming
  
    1. map (  دي list  علي كل حاجه داخل ال function  و بينفذ ال list  علي ال loop هو  كدا ب  )
  
       ```python
       names = ['Mohamed', 'Ahemd', 'Amr', 'Abdelmonem']
       # دي داله بتجيب عدد الحروف 
       def mylen(n):
           return len(n)
       # list بناخد function و ال    map دي استخدام ال
       # list بترجع بكل اللي ف  map ال   
       result = map(mylen, names)
       print(list(result))
       ```
  
       
  
    2. filter
  
       ```python
       names = ['Mohamed', 'Ahemd', 'Amr', 'Abdelmonem']
       # دي داله بتجيب عدد الحروف 
       def mylen(n):
           if len(n)>3:
              return len(n)
       # list بناخد function و ال    map دي استخدام ال    
       # list و كدا هي هترجع ب بعض الارقام يعني الداله مش بتتنفذ علي كل اللي داخل ال  
       result = filter(mylen, names)
       print(list(result))
       ```
  
       
  
    3. reduce
  
       ```python
       from functools import reduce
       
       numbers = list(range(1,100))
       def mysum(x,y):
           return x+y
       
       result = reduce(mysum, numbers)
       print(result)
       
       ```
  
       