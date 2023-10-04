# Ex. No: 4 Creating Procedures using PL/SQL

### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
SQL> CREATE TABLE emp( empid NUMBER,empname VARCHAR(10),dept VARCHAR(10), salary NUMBER);
SQL> set serveroutput on
SQL> CREATE OR REPLACE PROCEDURE emp_data AS
  2  BEGIN
  3  INSERT INTO emp(empid,empname,dept,salary)
  4  values(1,'dinesh','IT',10000);
  5  INSERT INTO emp(empid,empname,dept,salary)
  6  values(2,'BABU','clerk',10001);
  7  INSERT INTO emp(empid,empname,dept,salary)
  8  values(3,'naagu','manager',200000);
  9  COMMIT;
 10  FOR emp_rec IN (SELECT * FROM emp)LOOP
 11  DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
 12  END LOOP;
 13  END;
 14  /
```
```

### Output:

![WhatsApp Image 2023-10-04 at 22 44 45_99020878](https://github.com/RANJEETH17/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/120718823/680c1a08-91dd-4cd3-b001-8d6bba5e142d)








### Result:
THE PROGRAM HAS BEEN IMPLEMENTED SUCCESSFULLY
