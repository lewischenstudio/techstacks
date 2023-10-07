## Difference Between Trigger And Procedure in DBMS

#### Table of Contents

- [Procedures](#procedures)
- [Triggers](#triggers)
- [Difference between Triggers and Procedures](#difference-between-triggers-and-procedures)

### Procedures

A procedure is a combination of SQL statements written to perform specified
tasks. It helps in code re-usability and saves time and lines of code.

Advantages of Procedures:

- A Stored Procedure can be used as modular programming, which means that it can
  be created once, stored, and called multiple times as needed. This allows for
  speedier execution.
- Reduces network traffic
- Improving data security
- Easy to maintain because the stored procedure scripts are all in one place and
  hence, it is easy to update and track dependencies when schema changes occur.
- Testing can be carried out independent of the application.

### Triggers

A trigger is a special kind of procedure that executes only when some triggering
event such as INSERT, UPDATE, or DELETE operations occur in a table.

Advantages of Triggers:

- Protection of data
- Inhibits transactions that are not valid
- It also keeps the different tables in sync.
- Referential integrity is enforced with the use of triggers.
- Triggers can also be used in event logging and auditing.

### Difference between Triggers and Procedures

| S.No. |       Parameters       |                                                   Triggers                                                    |                                                              Procedures                                                               |
| :---: | :--------------------: | :-----------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------: |
|  1.   |         Basics         |    A Trigger is implicitly invoked whenever any event such as INSERT, DELETE, or UPDATE occurs in a TABLE.    | A Procedure is explicitly called by the user/application using statements or commands such as exec, EXECUTE, or simply procedure name |
|  2.   |         Action         |                   When an event occurs, a trigger helps to execute an action automatically.                   |                                   A procedure helps to perform a specified task when it is invoked.                                   |
|  3.   |      Define/call       | Only nesting of triggers can be achieved in a table. We cannot define/call a trigger inside another trigger.  |                                        We can define/call procedures inside another procedure.                                        |
|  4.   |         Syntax         |                  In a database, the syntax to define a trigger: CREATE TRIGGER TRIGGER_NAME                   |                           In a database, the syntax to define a procedure: CREATE PROCEDURE PROCEDURE_NAME                            |
|  5.   | Transaction statements |          Transaction statements such as COMMIT, ROLLBACK, and SAVEPOINT are not allowed in triggers.          |                           All transaction statements such as COMMIT and ROLLBACK are allowed in procedures.                           |
|  6.   |         Usage          | Triggers are used to maintain referential integrity by keeping a record of activities performed on the table. |                                Procedures are used to perform tasks defined or specified by the users.                                |
|  7.   |      Return value      |        We cannot return values in a trigger. Also, as an input, we cannot pass values as a parameter.         |                                We can return 0 to n values. However, we can pass values as parameters.                                |

[Content Source](https://www.geeksforgeeks.org/difference-between-trigger-and-procedure-in-dbms/)
