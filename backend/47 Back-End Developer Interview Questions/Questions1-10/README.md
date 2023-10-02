## Questions 1 - 10

#### Table of Contents

- [What is CAP theorem?](#what-is-cap-theorem)
- [What REST stands for?](#what-rest-stands-for)
- [What are NoSQL databases? What are the different types of NoSQL databases?](#what-are-nosql-databases-what-are-the-different-types-of-nosql-databases)
- [What do you understand by NoSQL databases? Explain.](#what-do-you-understand-by-nosql-databases-explain)
- [What is SQL injection?](#what-is-sql-injection)
- [What is meant by Continuous Integration?](#what-is-meant-by-continuous-integration)
- [How to mitigate the SQL injection risks?](#how-to-mitigate-the-sql-injection-risks)
- [Name some performance testing steps](#name-some-performance-testing-steps)
- [Name the difference between _Acceptance Test_ and _Functional Test_](#name-the-difference-between-acceptance-test-and-functional-test)
- [What are some advantages of using Go?](#what-are-some-advantages-of-using-go)

### What is CAP theorem?

The **CAP Theorem** for distributed computing was published by Eric Brewer. This
states that it is not possible for a distributed computer system to
simutaneously provide all three of the following guarantees:

1. _Consistency_ (all nodes see the same data even at the same time with
   concurrent updates)
2. _Availability_ (a guarantee that every request receives a response about
   whether it was successful or failed)
3. _Partition tolerance_ (the system continues to operate despite arbitrary
   message loss or failure of part of the system)

The CAP acronym corresponds to these guarantees. This theorem has created the
base for modern distributed computing approaches. Worlds most high volume
traffic companies (e.g. Amazon, Google, Facebook) use this as basis for deciding
their application architecture. It's important to understand that only two of
these three conditions can be guaranteed to be met by a system.

### What REST stands for?

_REST_ stands for REpresentational State Transfer. REST is web standards based
architecture and use HTTP Protocol for data communication. It revolves around
resource where every component is a resource and a resource is accessed by a
common interface using HTTP standard methods. REST was first introduced by Roy
Fielding in 2000.

### What are NoSQL databases? What are the different types of NoSQL databases?

A NoSQL database provides a mechanism for storage and retrieval of data that is
modeled in means other than tabular relations used in relational databases (like
SQL, Oracle, etc).

Types of NoSQL databases:

- Document Oriented
- Key Value
- Graph
- Column Oriented

### What do you understand by NoSQL databases? Explain.

At the present time, the internet is loaded with big data, big users, big
complexity, etc., and it is also becoming more complex day by day. NoSQL is
answer of all these problems. It is not a traditional database management
system, not even a relational database management system (RDBMS). NoSQL stands
for "Not Only SQL". NoSQL is a type of database that can handle and sort all
type of unstructured, messy and complicated data. It is just a new way to think
about the database.

### What is SQL injection?

Injection attacks stem from a lack of strict separation between program
instructions (i.e., code) and user-provided (or external) input. This allows an
attacker to inject malicious code into a data snippet.

_SQL injection_ is one of the most common types of injection attack. To carry it
out, an attacker provides malicious SQL statements through the application.

How to prevent:

- **Prepared statements with parametrized queries**
- **Stored procedures**
- **Input validation** - backlist validation and whitelist validation
- **Principle of least privilege** - Application accounts shouldn't assign DBA
  or admin type access onto the database server. This ensures that if an
  application is compromized, an attacker won't have the rights to the database
  through the compromized application.

### What is meant by Continuous Integration?

_Continuous Integration (CI)_ is a development practice that requires developers
to integrate code into a shared erpository several times a day. Each check-in is
then verified by an automated build, allowing teams to detect problems early.

### How to mitigate the SQL injection risks?

To mitigate SQL injection:

- **Prepared Statements with Parametrized Queries**: Always ensure that your SQL
  interpreter always able to differentiate between code and data. Never use
  dynamic queries which fail to find the difference code and data. Instead, use
  static SQL query and then pass in the external input as a parameter to query.
  Use of Prepared Statements (with Parametrized Queries) force developer to
  first define all the SQL code, and then pass in each parameter to the query
  later.
- **Use of Stored Procedures**: Stored Procedure is like a function in C where
  database administrator call it whenever he/she needs it. It is not completely
  mitigated SQL injection but definitely helps in reducing risks of SQL
  injection by avoiding dynamic SQL generation inside.
- **White List Input Validation**: Always use white list input validation and
  allow only pre-approved input by the developer. Never use blacklist approach
  as it is less secure than whitelist approach.
- **Escaping All User Supplied Input**
- **Enforcing Least Privilege**

### Name some performance testing steps

Some of the performance testing steps are:

- Identify the testing environment
- Identify performance metrics
- Plan and design performance tests
- Configure the test environment
- Implement your test design
- Execute tests
- Analyze, report, retest

### Name the difference between _Acceptance Test_ and _Functional Test_

- **Functional testing**: This is a _verification_ activity. Did we build a
  correctly working product? Does the software meet the business requirements? A
  functional test verifies that the product actually works as you (the develper)
  think it does.
- **Accepting testing**: This is a _validation_ activity. Did we build the right
  thing? Is this what the customer really needs? Acceptance tests verify the
  product actually solves the problem it was made to solve. This can best done
  by the user (customer), for instance performaing his/her tasks that the
  software assists with.

### What are some advantages of using Go?

**Go** is an attempt to introduce a new, concurrent, garbage-collected language
with fast compilation and the following benefits:

- It is possible to compile a large Go program in a few seconds on a single
  computer.
- Go provides a model for software construction that makes dependency analysis
  easy and avoids much of the overhead of C-style include files and libraries.
- Go's type system has no hierarchy, so no time is spent defining the
  relationships between types. Also, although Go has static types, the language
  attempts to make types feel lighter weight than in typical OO languages.
- Go is fully garbage-collected and provides fundamental support for concurrent
  execution and communication.
- By its design, Go proposes an approach for the construction of system software
  on multicore machines.
