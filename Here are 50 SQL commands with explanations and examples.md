

![sql cover](C:\Users\DELL\Downloads\sql cover.jpg)



















###  Here are 50 SQL commands with explanations and examples:



1. SELECT * FROM table_name; - Retrieves all records from the specified table.
   Example: SELECT * FROM employees;

2. UPDATE table_name SET column_name = value WHERE condition; - Updates records in the table based on the given condition.
   Example: UPDATE customers SET city = 'New York' WHERE customer_id = 101;

3. INSERT INTO table_name (column1, column2, ...) VALUES (value1, value2, ...); - Inserts new records with specified values into the table.
   Example: INSERT INTO products (product_id, product_name, price) VALUES (101, 'Laptop', 1000);

4. DELETE FROM table_name WHERE condition; - Deletes records from the table based on the given condition.
   Example: DELETE FROM orders WHERE order_status = 'Cancelled';

5. CREATE TABLE table_name (column1 datatype1, column2 datatype2, ...); - Creates a new table with specified column names and data types.
   Example: CREATE TABLE customers (customer_id INT, customer_name VARCHAR(50), email VARCHAR(100));

6. ALTER TABLE table_name ADD column_name datatype; - Adds a new column to the existing table.
   Example: ALTER TABLE employees ADD date_of_birth DATE;

7. DROP TABLE table_name; - Deletes the entire table from the database.
   Example: DROP TABLE products;

8. JOIN table1 ON table1.column = table2.column; - Combines data from two or more tables based on a related column.
   Example: SELECT orders.order_id, customers.customer_name FROM orders JOIN customers ON orders.customer_id = customers.customer_id;

9. GROUP BY column_name HAVING condition; - Groups rows based on a specific column and applies a condition on groups using aggregate functions.
   Example: SELECT country, COUNT(*) AS order_count FROM orders GROUP BY country HAVING order_count > 100;

10. ORDER BY column_name ASC/DESC; - Sorts the result set in ascending or descending order based on a column.
    Example: SELECT product_name, price FROM products ORDER BY price DESC;

11. DISTINCT column_name FROM table_name; - Retrieves unique values from the specified column.
    Example: SELECT DISTINCT city FROM customers;

12. BETWEEN value1 AND value2; - Filters results to include values within a specified range.
    Example: SELECT product_name FROM products WHERE price BETWEEN 500 AND 1000;

13. LIKE 'pattern'; - Performs a pattern match search using wildcards (% for multiple characters, _ for a single character).
    Example: SELECT product_name FROM products WHERE product_name LIKE 'Lap%';

14. IN (value1, value2, ...); - Filters results to include values that match any item in the list.
    Example: SELECT product_name FROM products WHERE category_id IN (1, 3, 5);

15. NOT IN (value1, value2, ...); - Filters results to exclude values that match any item in the list.
    Example: SELECT product_name FROM products WHERE category_id NOT IN (4, 6);

16. IS NULL; - Filters results to include only null values.
    Example: SELECT product_name FROM products WHERE description IS NULL;

17. IS NOT NULL; - Filters results to include only non-null values.
    Example: SELECT product_name FROM products WHERE description IS NOT NULL;

18. COUNT(column_name); - Returns the number of non-null values in the specified column.
    Example: SELECT COUNT(customer_id) AS customer_count FROM customers;

19. SUM(column_name); - Calculates the sum of values in the specified numeric column.
    Example: SELECT SUM(quantity) AS total_quantity FROM order_items;

20. AVG(column_name); - Calculates the average of values in the specified numeric column.
    Example: SELECT AVG(price) AS average_price FROM products;

21. MAX(column_name); - Retrieves the maximum value from the specified column.
    Example: SELECT MAX(salary) AS highest_salary FROM employees;

22. MIN(column_name); - Retrieves the minimum value from the specified column.
    Example: SELECT MIN(age) AS youngest_age FROM students;

23. UPPER(column_name); - Converts the values in the specified column to uppercase.
    Example: SELECT UPPER(first_name) AS uppercase_name FROM employees;

24. LOWER(column_name); - Converts the values in the specified column to lowercase.
    Example: SELECT LOWER(last_name) AS lowercase_name FROM customers;

25. CONCAT(string1, string2, ...); - Concatenates two or more strings together.
    Example: SELECT CONCAT(first_name, ' ', last_name) AS full_name FROM employees;

26. SUBSTRING(column_name, start_position, length); - Extracts a substring from the specified column.
    Example: SELECT SUBSTRING(description, 1, 50) AS short_description FROM products;

27. CASE WHEN condition THEN result ELSE other_result END; - Performs conditional logic in the SELECT statement.
    Example: SELECT product_name, CASE WHEN price > 1000 THEN 'Expensive' ELSE 'Affordable' END AS price_category FROM products;

28. AS alias_name; - Assigns an alias to a column or table.
    Example: SELECT customer_id AS ID, customer_name AS Name FROM customers;

29. INNER JOIN table2 ON table1.column = table2.column; - Retrieves matching records from both tables.
    Example: SELECT orders.order_id, customers.customer_name FROM orders INNER JOIN customers ON orders.customer_id = customers.customer_id;

30. LEFT JOIN table2 ON table1.column = table2.column; - Retrieves all records from the left table and matching records from the right table.
    Example: SELECT customers.customer_name, orders.order_id FROM customers LEFT JOIN orders ON customers.customer_id = orders.customer_id;

31. RIGHT JOIN table2 ON table1.column = table2.column; - Retrieves all records from the right table and matching records from the left table.
    Example: SELECT employees.employee_name, departments.department_name FROM employees RIGHT JOIN departments ON employees.department_id = departments.department_id;

32. FULL OUTER JOIN table2 ON table1.column = table2.column; - Retrieves all records when there is a match in either the left or right table.
    Example: SELECT customers.customer_name, orders.order_id FROM customers FULL OUTER JOIN orders ON customers.customer_id = orders.customer_id;

33. UNION; - Combines the results of two or more SELECT statements (removing duplicates).
    Example: SELECT product_name FROM products WHERE category_id = 1 UNION SELECT product_name FROM products WHERE category_id = 2;

34. UNION ALL; - Combines the results of two or more SELECT statements (keeping duplicates).
    Example: SELECT product_name FROM products WHERE category_id = 1 UNION ALL SELECT product_name FROM products WHERE category_id = 2;

35. EXISTS (SELECT * FROM table_name WHERE condition); - Checks for the existence of rows in a subquery.
    Example: SELECT customer_name FROM customers WHERE EXISTS (SELECT * FROM orders WHERE customers.customer_id = orders.customer_id);

36. ANY/SOME (SELECT column_name FROM table_name WHERE condition); - Compares a value to a set of values returned by a subquery.
    Example: SELECT product_name FROM products WHERE price > ANY (SELECT price FROM products WHERE category_id = 3);

37. ALL (SELECT column_name FROM table_name WHERE condition); - Compares a value to all values returned by a subquery.
    Example: SELECT product_name FROM products WHERE price > ALL (SELECT price FROM

 products WHERE category_id = 1);

38. GROUP_CONCAT(column_name SEPARATOR 'delimiter'); - Concatenates values of a column into a single string with a specified delimiter.
    Example: SELECT customer_id, GROUP_CONCAT(order_id SEPARATOR ', ') AS order_list FROM orders GROUP BY customer_id;

39. HAVING aggregate_function(condition); - Filters groups of rows based on aggregate function results.
    Example: SELECT customer_id, COUNT(order_id) AS order_count FROM orders GROUP BY customer_id HAVING order_count > 3;

40. CREATE INDEX index_name ON table_name (column_name); - Creates an index on a column to improve query performance.
    Example: CREATE INDEX idx_product_name ON products (product_name);

41. DROP INDEX index_name ON table_name; - Removes an index from the table.
    Example: DROP INDEX idx_product_name ON products;

42. CREATE VIEW view_name AS SELECT column1, column2, ... FROM table_name WHERE condition; - Creates a virtual table based on the SELECT statement.
    Example: CREATE VIEW top_customers AS SELECT customer_id, customer_name FROM customers WHERE total_purchase > 1000;

43. DROP VIEW view_name; - Deletes the specified view from the database.
    Example: DROP VIEW top_customers;

44. BEGIN; - Starts a transaction block.
    Example: BEGIN;

45. COMMIT; - Saves all changes made in the current transaction block.
    Example: COMMIT;

46. ROLLBACK; - Discards all changes made in the current transaction block.
    Example: ROLLBACK;

47. GRANT permissions ON table_name TO user_name; - Gives specific permissions on a table to a user.
    Example: GRANT SELECT, INSERT ON employees TO john_doe;

48. REVOKE permissions ON table_name FROM user_name; - Removes specific permissions on a table from a user.
    Example: REVOKE DELETE ON orders FROM jane_smith;

49. CREATE DATABASE database_name; - Creates a new database.
    Example: CREATE DATABASE my_database;

50. USE database_name; - Switches to the specified database for executing queries.
    Example: USE my_database;

هذه قائمة ببعض الأوامر الشائعة في لغة SQL مع الشرح وأمثلة لكل منها. يمكنك استخدام هذه الأوامر للتعامل مع قواعد البيانات واستعادة البيانات أو تحديثها أو حذفها أو إجراء عمليات أخرى تتعلق بإدارة البيانات في النظام الخاص بك.































### مع الشرح والأمثلة باللغة العربية

1. SELECT * FROM اسم_الجدول; - يسترجع كل السجلات من الجدول المحدد.
   مثال: SELECT * FROM الموظفين;

2. UPDATE اسم_الجدول SET اسم_العمود = قيمة WHERE الشرط; - يقوم بتحديث السجلات في الجدول استنادًا إلى الشرط المعطى.
   مثال: UPDATE العملاء SET المدينة = 'نيويورك' WHERE رقم_العميل = 101;

3. INSERT INTO اسم_الجدول (العمود1 ، العمود2 ، ...) VALUES (قيمة1 ، قيمة2 ، ...); - يقوم بإدراج سجلات جديدة بقيم محددة في الجدول.
   مثال: INSERT INTO المنتجات (رقم_المنتج ، اسم_المنتج ، السعر) VALUES (101 ، 'لابتوب' ، 1000);

4. DELETE FROM اسم_الجدول WHERE الشرط; - يحذف السجلات من الجدول استنادًا إلى الشرط المعطى.
   مثال: DELETE FROM الطلبات WHERE حالة_الطلب = 'ملغى';

5. CREATE TABLE اسم_الجدول (العمود1 نوع_البيانات1 ، العمود2 نوع_البيانات2 ، ...); - ينشئ جدولًا جديدًا بأسماء الأعمدة وأنواع البيانات المحددة.
   مثال: CREATE TABLE العملاء (رقم_العميل INT ، اسم_العميل VARCHAR(50) ، البريد_الإلكتروني VARCHAR(100));

6. ALTER TABLE اسم_الجدول ADD اسم_العمود نوع_البيانات; - يضيف عمودًا جديدًا إلى الجدول الحالي.
   مثال: ALTER TABLE الموظفين ADD تاريخ_الميلاد DATE;

7. DROP TABLE اسم_الجدول; - يحذف الجدول بأكمله من قاعدة البيانات.
   مثال: DROP TABLE المنتجات;

8. JOIN اسم_الجدول1 ON اسم_الجدول1.العمود = اسم_الجدول2.العمود; - يدمج البيانات من جدولين أو أكثر بناءً على عمود ذي صلة.
   مثال: SELECT رقم_الطلب ، اسم_العميل FROM الطلبات JOIN العملاء ON الطلبات.رقم_العميل = العملاء.رقم_العميل;

9. GROUP BY اسم_العمود HAVING الشرط; - يقوم بتجميع الصفوف استنادًا إلى عمود محدد وتطبيق شرط على المجموعات باستخدام وظائف التجميع.
   مثال: SELECT البلد ، COUNT(*) AS عدد_الطلبيات FROM الطلبات GROUP BY البلد HAVING عدد_الطلبيات > 100;

10. ORDER BY اسم_العمود ASC/DESC; - يقوم بفرز مجموعة النتائج بترتيب تصاعدي أو تنازلي بناءً على عمود.
    مثال: SELECT اسم_المنتج ، السعر FROM المنتجات ORDER BY السعر DESC;

11. DISTINCT اسم_العمود FROM اسم_الجدول; - يسترجع قيم فريدة من العمود المحدد.
    مثال: SELECT DISTINCT المدينة FROM العملاء;

12. BETWEEN قيمة1 وقيمة2; - يقوم بتصفية النتائج لتشمل القيم ضمن نطاق محدد.
    مثال: SELECT اسم_المنتج FROM المنتجات WHERE السعر BETWEEN 500 و 1000;

13. LIKE 'نمط'; - يقوم بالبحث باستخدام نمط يحتوي على علامات الاستبدال (% للحروف المتعددة ، _ لحرف واحد).
    مثال: SELECT اسم_المنتج FROM المنتجات WHERE اسم_المنتج LIKE 'لاب%';

14. IN (قيمة1 ، قيمة2 ، ...); - يقوم بتصفية النتائج لتشمل القيم التي تطابق أي عنصر في القائمة.
    مثال: SELECT اسم_المنتج FROM المنتجات WHERE رقم_الفئة IN (1 ، 3 ، 5);

15. NOT IN (قيمة1 ، قيمة2 ، ...); - يقوم بتصفية النتائج لاستبعاد القيم التي تطابق أي عنصر في القائمة.
    مثال: SELECT اسم_المنتج FROM الم

نتجات WHERE رقم_الفئة NOT IN (4 ، 6);

16. IS NULL; - يقوم بتصفية النتائج لاستبعاد القيم الفارغة (NULL).
    مثال: SELECT اسم_المنتج FROM المنتجات WHERE الوصف IS NULL;

17. IS NOT NULL; - يقوم بتصفية النتائج لاستبعاد القيم غير الفارغة (NOT NULL).
    مثال: SELECT اسم_المنتج FROM المنتجات WHERE الوصف IS NOT NULL;

18. COUNT(اسم_العمود); - يعيد عدد القيم غير الفارغة في العمود المحدد.
    مثال: SELECT COUNT(رقم_العميل) AS عدد_العملاء FROM العملاء;

19. SUM(اسم_العمود); - يحسب مجموع القيم في العمود الرقمي المحدد.
    مثال: SELECT SUM(الكمية) AS الكمية_الإجمالية FROM عناصر_الطلب;

20. AVG(اسم_العمود); - يحسب المتوسط الحسابي للقيم في العمود الرقمي المحدد.
    مثال: SELECT AVG(السعر) AS متوسط_السعر FROM المنتجات;

21. MAX(اسم_العمود); - يسترجع القيمة الأقصى من العمود المحدد.
    مثال: SELECT MAX(الراتب) AS أعلى_راتب FROM الموظفين;

22. MIN(اسم_العمود); - يسترجع القيمة الأدنى من العمود المحدد.
    مثال: SELECT MIN(العمر) AS أصغر_عمر FROM الطلاب;

23. UPPER(اسم_العمود); - يقوم بتحويل القيم في العمود المحدد إلى حروف كبيرة (أحرف كبيرة).
    مثال: SELECT UPPER(الاسم_الأول) AS اسم_كبير_الأحرف FROM الموظفين;

24. LOWER(اسم_العمود); - يقوم بتحويل القيم في العمود المحدد إلى حروف صغيرة (أحرف صغيرة).
    مثال: SELECT LOWER(الاسم_الأخير) AS اسم_صغير_الأحرف FROM العملاء;

25. CONCAT(سلسلة1 ، سلسلة2 ، ...); - يقوم بدمج سلسلتين أو أكثر معًا.
    مثال: SELECT CONCAT(الاسم_الأول ، ' ' ، الاسم_الأخير) AS الاسم_الكامل FROM الموظفين;

26. SUBSTRING(اسم_العمود ، موضع_البداية ، الطول); - يستخرج سلسلة فرعية من العمود المحدد.
    مثال: SELECT SUBSTRING(الوصف ، 1 ، 50) AS وصف_قصير FROM المنتجات;

27. CASE WHEN الشرط THEN النتيجة ELSE النتيجة_الأخرى END; - ينفذ منطق مشروط في جملة SELECT.
    مثال: SELECT اسم_المنتج ، CASE WHEN السعر > 1000 THEN 'مكلف' ELSE 'معقول' END AS فئة_السعر FROM المنتجات;

28. AS اسم_الاسم; - يعين اسمًا بديلًا للعمود أو الجدول.
    مثال: SELECT رقم_العميل AS الرقم_التعريفي ، اسم_العميل AS الاسم FROM العملاء;

29. INNER JOIN اسم_الجدول2 ON اسم_الجدول1.العمود = اسم_الجدول2.العمود; - يسترجع السجلات المتطابقة من كلا الجدولين.
    مثال: SELECT رقم_الطلب ، اسم_العميل FROM الطلبات INNER JOIN العملاء ON الطلبات.رقم_العميل = العملاء.رقم_العميل;

30. LEFT JOIN اسم_الجدول2 ON اسم_الجدول1.العمود = اسم_الجدول2.العمود; - يسترجع كل السجلات من الجدول الأيسر والسجلات المتطابقة من الجدول الأيمن.
    مثال: SELECT اسم_العميل ، رقم_الطلب FROM العملاء LEFT JOIN الطلبات ON العملاء.رقم_العميل = الطلبات.رقم_العميل;

31. RIGHT JOIN اسم_الجدول2 ON اسم_الجدول1.العمود = اسم_الجدول2.العمود; - يسترجع كل السجلات من الجدول الأيمن والسجلات المتطابقة من الجدول الأيسر.
    مثال: SELECT اسم_الموظف ، اسم_القسم FROM الموظفين RIGHT JOIN الأقسام ON الموظفين.رقم

_القسم = الأقسام.رقم_القسم;

32. FULL OUTER JOIN اسم_الجدول2 ON اسم_الجدول1.العمود = اسم_الجدول2.العمود; - يسترجع كل السجلات عند وجود تطابق في أي من الجدولين.
    مثال: SELECT اسم_العميل ، رقم_الطلب FROM العملاء FULL OUTER JOIN الطلبات ON العملاء.رقم_العميل = الطلبات.رقم_العميل;

33. UNION; - يدمج نتائج اثنين أو أكثر من جمل SELECT (مع إزالة التكرار).
    مثال: SELECT اسم_المنتج FROM المنتجات WHERE رقم_الفئة = 1 UNION SELECT اسم_المنتج FROM المنتجات WHERE رقم_الفئة = 2;

34. UNION ALL; - يدمج نتائج اثنين أو أكثر من جمل SELECT (مع الاحتفاظ بالتكرار).
    مثال: SELECT اسم_المنتج FROM المنتجات WHERE رقم_الفئة = 1 UNION ALL SELECT اسم_المنتج FROM المنتجات WHERE رقم_الفئة = 2;

35. EXISTS (SELECT * FROM اسم_الجدول WHERE الشرط); - يتحقق من وجود صفوف في الاستعلام الفرعي.
    مثال: SELECT اسم_العميل FROM العملاء WHERE EXISTS (SELECT * FROM الطلبات WHERE العملاء.رقم_العميل = الطلبات.رقم_العميل);

36. ANY/SOME (SELECT اسم_العمود FROM اسم_الجدول WHERE الشرط); - يقارن قيمة مع مجموعة من القيم المُرجَعة بواسطة الاستعلام الفرعي.
    مثال: SELECT اسم_المنتج FROM المنتجات WHERE السعر > ANY (SELECT السعر FROM المنتجات WHERE رقم_الفئة = 3);

37. ALL (SELECT اسم_العمود FROM اسم_الجدول WHERE الشرط); - يقارن قيمة مع كل القيم المُرجَعة بواسطة الاستعلام الفرعي.
    مثال: SELECT اسم_المنتج FROM المنتجات WHERE السعر > ALL (SELECT السعر FROM المنتجات WHERE رقم_الفئة = 1);

38. GROUP_CONCAT(اسم_العمود مفصول_بواسطة 'الفاصلة'); - يدمج قيم العمود في سلسلة واحدة باستخدام فاصلة محددة.
    مثال: SELECT رقم_العميل ، GROUP_CONCAT(رقم_الطلب مفصول_بواسطة ', ') AS قائمة_الطلب FROM الطلبات GROUP BY رقم_العميل;

39. HAVING وظيفة_التجميع(الشرط); - يصفي مجموعات الصفوف بناءً على نتائج وظيفة التجميع.
    مثال: SELECT رقم_العميل ، COUNT(رقم_الطلب) AS عدد_الطلبات FROM الطلبات GROUP BY رقم_العميل HAVING عدد_الطلبات > 3;

40. CREATE INDEX اسم_الفهرس ON اسم_الجدول (اسم_العمود); - ينشئ فهرسًا على العمود لتحسين أداء الاستعلام.
    مثال: CREATE INDEX idx_اسم_المنتج ON المنتجات (اسم_المنتج);

41. DROP INDEX اسم_الفهرس ON اسم_الجدول; - يقوم بإزالة فهرس من الجدول.
    مثال: DROP INDEX idx_اسم_المنتج ON المنتجات;

42. CREATE VIEW اسم_العرض AS SELECT العمود1 ، العمود2 ، ... FROM اسم_الجدول WHERE الشرط; - ينشئ جدولًا افتراضيًا استنادًا إلى جملة SELECT.
    مثال: CREATE VIEW العملاء_المميزين AS SELECT رقم_العميل ، اسم_العميل FROM العملاء WHERE المشتريات_الكلية > 1000;

43. DROP VIEW اسم_العرض; - يقوم بحذف الجدول الافتراضي المحدد من قاعدة البيانات.
    مثال: DROP VIEW العملاء_المميزين;

44. BEGIN; - يبدأ كتلة معاملة جديدة.
    مثال: BEGIN;

45. COMMIT; - يحفظ جميع التغييرات التي تم إجراؤها في كتلة المعاملات الحالية.
    مثال: COMMIT;

46. ROLLBACK; - يلغي جميع التغييرات التي تم إجراؤها في كتلة المعاملات الحالية.
    مثال: ROLLBACK;

47

. GRANT الصلاحيات ON اسم_الجدول TO اسم_المستخدم; - يمنح صلاحيات محددة على الجدول للمستخدم.
    مثال: GRANT SELECT ، INSERT ON الموظفين TO john_doe;

48. REVOKE الصلاحيات ON اسم_الجدول FROM اسم_المستخدم; - يزيل الصلاحيات المحددة على الجدول من المستخدم.
    مثال: REVOKE DELETE ON الطلبات FROM jane_smith;

49. CREATE DATABASE اسم_قاعدة_البيانات; - ينشئ قاعدة بيانات جديدة.
    مثال: CREATE DATABASE قاعدة_البيانات_الخاصة_بي;

50. USE اسم_قاعدة_البيانات; - يقوم بالتبديل إلى قاعدة البيانات المحددة لتنفيذ الاستعلامات.
    مثال: USE قاعدة_البيانات_الخاصة_بي;