## Questions Set B

#### Table of Contents

- [What are some advantages of using Go?](#what-are-some-advantages-of-using-go)
- [What are the advantages of Web Services?](#what-are-the-advantages-of-web-services)
- [What are the benefits of using Go programming?](#what-are-the-benefits-of-using-go-programming)
- [What does Containerization mean?](#what-does-containerization-mean)
- [Why would You Opt For Microservices Architecture?](#why-would-you-opt-for-microservices-architecture)
- [Name some Performance Testing best practices](#name-some-performance-testing-best-practices)
- [What do you mean by High Availability (HA)?](#what-do-you-mean-by-high-availability-ha)
- [What is ACID property of a system?](#what-is-acid-property-of-a-system)
- [What is Sticky Session Load Balancing? What do you mean by "Session Affinity"?](#what-is-sticky-session-load-balancing-what-do-you-mean-by-session-affinity)
- [What are disadvantages of REST web services?](#what-are-disadvantages-of-rest-web-services)

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

### What are the advantages of Web Services?

Some of the advatanges of web services are

- **Interoperability**: Web services are accessible over network and runs on
  HTTP/SOAP protocol and uses XML/JSON to transport data, hence it can be
  developed in any programming language. Web service can be written in Java
  programming and client can be PHP and vice versa.
- **Reusability**: One web service can be used by many client applications at
  the same time.
- **Loose Coupling**: Web services client code is totally independent with
  server code, so we have achieved loose coupling in our application.
- **Easy to deploy and integrate**: just run web applications.
- **Multiple service versions** can be running at the same time.

### What are the benefits of using Go programming?

Following are the benefits of using Go programming:

- Support for environment adopting patterns similar to dynamic languages. For
  example, type inference (`x := 0` is valid declaration of a variable `x` of
  type `int`).
- Compilation time is fast.
- In built concurrency support: light-weight processes (via goroutines),
  channels, select statement.
- Conciseness, Simplicity, and Safty.
- Support for Interfaces and Type embedding.
- The go compiler supports static linking. All the go code can be statically
  linked into one big fat binary and it can be deployed in cloud servers easily
  without worrying about dependencies.

### What does Containerization mean?

_Containerization_ is a type of _virtualization_ strategy that emerged as an
alternative to traditional hypervisor-based virtualization.

In containerization, the operating system is shared by the different containers
rather than cloned for each virtual machine. For example Docker provides a
container virtualization platform that serves as a good alternative to
hypervisor-based arrangements.

### Why would You Opt For Microservices Architecture?

There are plenty of pros that are offered by Microservices architecture. Here
are a few of them:

- Microservices can adapt easily to other frameworks or technologies.
- Failure of a single process does not affect the entire system.
- Provides support to big enterprises as well as small teams.
- Can be deployed independently and in relatively less time.

### Name some Performance Testing best practices

- Test as early as possible in development
- Conduct multiple performance tests to ensure consistent findings and determine
  metrics averages
- Test the individual software units separately as well as together
- Baseline measurements provide a starting point for determining success or
  failure
- Performance tests are best conducted in test environments taht are as close to
  the production systems as possible
- Isolate the performance test environment from the environment used for quality
  assurance testing
- Keep the test environment as consistent as possible
- Calculating averages will deliver actionable metrics. There is value in
  tracking outliers alos. Those extreme measurements could reveal possible
  failures.

### What do you mean by High Availability (HA)?

**Availability** means the availability of the application user to access the
system. If a user cannot access the application, it is assumed unavailable. High
Availability means the application will be available, without interruption.
Using redundant server nodes without clustering in a common way to achieve
higher level of availability in web applications.

Availability is commonly expressed as a percentage of uptime in a given year.

### What is ACID property of a system?

_ACID_ is an acronym which is commonly used to define the properties of a
relational database system. It stands for following terms

- **Atomicity** -- This property guarantees that if one part of the transaction
  fails, the entire transaction will fail, and the database state will be left
  unchanged.
- **Consistency** -- This property ensures that any transaction will bring the
  database from one valid state to another.
- **Isolation** -- This property ensures that the concurrent execution of
  transactions result in a system state that would be obtained if transactions
  were executed serially.
- **Durability** -- It means that once a transaction has been committed, it will
  remain so, even in the event of power loss.

### What is Sticky Session Load Balancing? What do you mean by "Session Affinity"?

_Sticky session_ or _session affinity technique_ is another popular load
balancing technique that requires a user session to be always served by an
allocated machine.

In a load balanced server application where user information is stored in
session, it will be required to keep the session data available to all machines.
This can be avoided by always serving a particular user session request from one
machine. The machine is associated with a session as soon as the session is
created. All the requests in a particular session are always redirected to the
associated machine. This ensures the user data is only at one machine and load
is also shared.

This is typically done by using SessionId cookie. The cookie is sent to the
client for the first request and every subsequent request by client must be
containing that same cookie to identify the session.

**What are the issues with Sticky Session?**

There are few issues that youmay face with this approach

- The client browser may not support cookies, and your load balancer will not be
  able to identify if a request belongs to a session. This cause strange
  behavior for the users who use no cookie based browsers.
- In case one of the machine fails or goes down, the user information (served by
  that machine) will be lost and there will be no way to recover user session.

### What are disadvantages of REST web services?

Some of the disadvantages of REST are:

- Since there is no contract defined between service and client, it has to be
  communicated through other means such as documentation or emails.
- Since it works on HTTP, there can't be asynchronous calls.
- Sessions can't be maintained.
