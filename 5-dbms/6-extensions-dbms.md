# Chapter -6 Extensions of DBMS

The extension of DBMS is the extension to the schema which means when we are able to edit the tuples of the relation at any given instance. The extension is dependent on time i.e when we update, delete or insert data in the tuple then the extension gets updated. To perform such operations we use different types of languages like SQL, MySQL etc.

## SQL As A Programming Language
SQL (Structured Query Language) is a database management language for relational databases. SQL itself is not a programming language, but its standard allows creating procedural extensions for it, which extends it to the functionality of a mature programming language. The language was developed in 1970th under the name “SEQUEL” for database management system (DBMS) called System R. It was renamed to “SQL” later to avoid trademarks conflict.

SQL was first released for commercial purposes in 1979, implemented in Oracle V2.

### SQL/PSM
SQL/PSM (Structured Query Language/Persistent Stored Modules) is an ISO standard mainly defining an extension of SQL with a procedural language for use in stored procedures. It also defines an information schema (metadata) for stored procedures. SQL/PSM is one language in which methods for the SQL:1999 structured types can be defined. SQL/PSM standardizes procedural extensions for SQL, including flow of control, condition handling, statement condition signals and re-signals, cursors and local variables, and assignment of expressions to variables and parameters. 

### PL/SQL
PL/SQL is a combination of SQL along with the procedural features of programming languages. It was developed by Oracle Corporation in the early 90's to enhance the capabilities of SQL. PL/SQL is one of three key programming languages embedded in the Oracle Database, along with SQL itself and Java. The basic construct in PL/SQL is a block. In a block, constant and variables can be declared. Statement in PL/SQL block include SQL statements, control structures(loops), conditional statements (if-then-else) exception handling and many others.

## Control Statement


### 1. If Statement
PL/SQL supports the programming language features like conditional statements and iterative statements. Its programming constructs are similar to how you use in programming languages like Java and C++.

There are different syntaxes for the IF-THEN-ELSE statement.

 **Syntax1:** (IF-THEN statement):

>IF condition   
THEN   
Statement: {It is executed when condition is true}  
END IF;  

This syntax is used when you want to execute statements only when condition is TRUE.

**Syntax2:** (IF-THEN-ELSE statement):

>IF condition   
THEN  
   {...statements to execute when condition is TRUE...}  
ELSE  
   {...statements to execute when condition is FALSE...}  
END IF;   

This syntax is used when you want to execute one set of statements when condition is TRUE or a different set of statements when condition is FALSE.

**Syntax3:** (IF-THEN-ELSIF statement):

>IF condition1   
THEN  
   {...statements to execute when condition1 is TRUE...}  
ELSIF condition2   
THEN  
   {...statements to execute when condition2 is TRUE...}  
END IF;  

This syntax is used when you want to execute one set of statements when condition1 is TRUE or a different set of statements when condition2 is TRUE.

**Syntax4:** (IF-THEN-ELSIF-ELSE statement):

>IF condition1   
THEN  
   {...statements to execute when condition1 is TRUE...}  
ELSIF condition2   
THEN  
   {...statements to execute when condition2 is TRUE...}  
ELSE  
   {...statements to execute when both condition1 and condition2 are FALSE...}  
END IF;  

It is the most advance syntax and used if you want to execute one set of statements when condition1 is TRUE, a different set of statement when condition2 is TRUE or a different set of statements when both the condition1 and condition2 are FALSE.

### 2.  Exit Loop Statement

PL/SQL exit loop is used when a set of statements is to be executed at least once before the termination of the loop. There must be an EXIT condition specified in the loop, otherwise the loop will get into an infinite number of iterations. After the occurrence of EXIT condition, the process exits the loop. **Syntax:**
>LOOP   
   statements;   
   EXIT;   
   { or EXIT WHEN condition; }  
END LOOP;  

### 3. While Loop
PL/SQL while loop is used when a set of statements has to be executed as long as a condition is true, the While loop is used. The condition is decided at the beginning of each iteration and continues until the condition becomes false. **Syntax:**
>WHILE (condition)   
 LOOP statements;   
END LOOP;  

### 4. FOR Loop
PL/SQL for loop is used when when you want to execute a set of statements for a predetermined number of times. The loop is iterated between the start and end integer values. The counter is always incremented by 1 and once the counter reaches the value of end integer, the loop ends. **Syntax:**
>FOR counter IN initial_value .. final_value LOOP  
  LOOP statements;   
END LOOP;  
{ initial_value : Start integer value      
final_value : End integer value }


### 5. GoTo Statement
In PL/SQL, GOTO statement makes you able to get an unconditional jump from the GOTO to a specific executable statement label in the same subprogram of the PL/SQL block.

Here the label declaration which contains the label_name encapsulated within the << >> symbol and must be followed by at least one statement to execute. **Syntax:**
>GOTO label_name;  
 ..  
..  
<<label_name>>  
Statement;  