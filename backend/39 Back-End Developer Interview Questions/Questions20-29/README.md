## Questions 21 - 30

#### Table of Contents

- [What are the DRY and DIE principles?](#what-are-the-dry-and-die-principles)
- [What are the difference between _Clustered_ and _Non-clustered_ index?](#what-are-the-difference-between-clustered-and-non-clustered-index)
- [What are the differences between _Continuous Integration, Continuous Delivery_](#what-are-the-differences-between-continuous-integration-continuous-delivery-and-continuous-deployment)
  and _Continuous Deployment_?
- [What is the difference between Monolithic, SOA and Microservices Architecture?](#what-is-the-difference-between-monolithic-soa-and-microservices-architecture)
- [What is the difference between `JSON` and `UNION`?](#what-is-the-difference-between-json-and-union)
- [What is the difference between `WHERE` clause and `HAVING` clause?](#what-is-the-difference-between-where-clause-and-having-clause)
- [Explain what is the API Gateway pattern](#explain-what-is-the-api-gateway-pattern)
- [How does SSL/TSL work?](#how-does-ssltsl-work)
- [How does _B-trees Index_ work?](#how-does-b-trees-index-work)
- [What do you understand by Distributed Transaction?](#what-do-you-understand-by-distributed-transaction)

### What are the DRY and DIE principles?

In software engineering, **Don't Repeat Yourself (DRY)** or **Duplication is
Evil (DIE)** is a principle of software development.

### What are the difference between _Clustered_ and _Non-clustered_ index?

- With a **Clustered** index, the rows are stored **physically** on the disk in
  the same order as the index. Therefore, there can be only one clustered index.
  A clustered index means you are telling the database to store close values
  actually close to one another on the disk.
- With a **Non-Clustered** index, there is a second list that has **pointers**
  to the physical rows. You can have many non clustered indices, although each
  new index will increase the time it takes to write new records.
- It is generally _fast to read_ from **clustered** index if you want to get
  back all the columns. You don't have to go first to the index and then to the
  table.
- _Writing_ to a table with a **clustered** index can be _slower_, if there is a
  need to rearrange the data.

### What are the differences between _Continuous Integration, Continuous Delivery_ and _Continuous Deployment_?

- Developers practicing **continuous integration** merge their changes back to
  the main branch as often as possible. By doing so, you avoid the integration
  hell that usually happens when people wait for release day to merge their
  changes into the release branch.
- **Continuous delivery** is an extension of continous integration to make sure
  that you can release new changes to your customers quickly in a sustainable
  way. This means that on top of having automated your testing, you also have
  automated your release process and you can deploy your application at any
  point of the time by clicking on a button.
- **Continuous deployment** goes one step further than continuous delivery. With
  this practice, every change that passes all stages of your production pipeline
  is released to your customers. There is no human intervention, and only a
  failed test will prevent a new change to be deployed to production.

### What is the difference between Monolithic, SOA and Microservices Architecture?

- **Monolithic Architecture** is similar to a big container wherein all the
  software components of an application are assembled together and tightly
  packaged.
- A **Service-Oriented Architecture** is a collection of services which
  communicate with each other. The communication can involve either simple data
  passing or it could involve two or more services coordinating some activity.
- **Microservice Architecture** is an architectural style that structures an
  application as a collection of small autonomous services, modeled around a
  business domain.

### What is the difference between `JSON` and `UNION`?

They are completely different operations.

`UNION` puts lines from queries.

```sql
SELECT 23 AS bah
UNION
SELECT 45 AS bah;
```

```
Output
+------+
|  bah |
+------+
|  23  |
|  45  |
+------+
```

`JOIN` makes a _cartesian_ product and subsets it.

```sql
SELECT * FROM
(SELECT 23 AS bah) AS foo
JOIN
(SELECT 45 AS bah) AS BAR
ON (33=33);
```

```
Output
+------+------+
|  foo |  bar |
+------+------+
|  23  |  45  |
+------+------+
```

### What is the difference between `WHERE` clause and `HAVING` clause?

`WHERE` clause introduces a condition on _individual_ rows.

`HAVING` clause introduces a condition on _aggregations_, i.e. results of
selection where a single result, such as count, average, min, max, or sum, has
been produced from _multiple_ rows. Your query calls for a second kind of
condition (i.e. a condition on an aggregation) hence `HAVING` works correctly.

As a rule of thumb, use `WHERE` before `GROUP BY` and `HAVING` after `GROUP BY`.
It is a rather primitive rule, but it is useful in more than 90% of the cases.

```sql
SELECT L.LectID, Fname, Lname
FROM Lecturers L
JOIN Lecturers_Specialization S ON L.LectID=S.LectID
GROUP BY L.LectID, Fname, Lname
HAVING COUNT (S.Expertise)>=ALL
(SELECT COUNT(Expertise) FROM Lecturers_Specialization GROUP BY LectID)
```

### Explain what is the API Gateway pattern

An **API Gateway** is a server that is the single entry point into the system.
It is similar to the Facade pattern from object-oriented design. The API Gateway
encapsulates the internal system architecture and provides an API that is
tailored to each client. It might have other responsibilities such as
authentication, monitoring, load balancing, caching, request shaping and
management, and static response handling.

A major benefit of using an API Gateway is that it encapsulates the internal
structure of the application. Rather than having to invoke specific services,
clients simply talk to the gateway.

### How does SSL/TLS work?

**SSL** (and its successor, **TLS**) is a protocol that operates directly on top
of TCP. This way, protocols on higher layers (such as HTTP) can be left
unchanged while still providing a secure connection. Underneath the SSL layer,
HTTP is identical to HTTPS. When using SSL/TLS correctly, all an attacker can
see on the cable is which IP and port you are connected to, roughly how much
data you are sending, and what encryption and compression is used. He can also
terminate the connection, but both sides will know that the connection has been
interrupted by a third party.

1. After building a TCP connection, the SSL handshake is started by the client
   that sends a number of specifications:
   - which version of SSL/TLS it is running.
   - what ciphersuites it wants to use, and
   - what compression methods it wants to use.
2. The server checks what the highest SSL/TLS version is supported by them both,
   picks a ciphersuite from one of the client's options (if it supports one),
   and optionally picks a compression method.
3. After this the basic setup is done, the server sends it _certificate_. This
   certificate must be trusted by either the client itself or a party that the
   client trusts. Having verified the certificate and being certain this server
   really is who he claims (and not a man in the middle), a key is exchanged.
   The client tells the server that from now on, all communication will be
   encrypted, and sends an encrypted and authenticated message to the server.
4. The server verifies that the MAC (used for authentication) is correct, and
   that the message can be correctly decrypted. It then returns a message, which
   the client verifies as well.
5. The handshake is now finished, and the two hosts can communicate securely.

### How does _B-trees Index_ work?

The main reason for the existence of **B-Tree Index** is to better utilize the
behavior of devices that read and write large chunks of data. Two properties are
important to make the B-Tree better than binary trees when data has to be stored
on disk:

- Access to disk is really slow (compared to memory or caches, random access to
  data on disk is orders of magnitude slower); and
- Every single read causes a whole sector to be loaded from the drive --
  assuming a sector size is 4K, this means 1000 integers, or tens of some larger
  objects you're storing.

Hence, we can use the pros of the second fact, while also minimizing the cons -
i.e. number of disk accesses.

So, instead of just storing a single number in every node that tells us if we
should continue to the left or to the right, we can create bigger index that
tells us if we should continue to the first 1/100, to the second or to the left
99-th (imagine books in a library sorted by their first letter, then by the
second, and so on). As long as all this data fits on a single sector, it will be
loaded anyway, so we might as well use it completely.

This results in roughly $log_bN$ lookups, where `N` is the number of records.
This number, while asymptotically the same as $log_2N$, is actually a few times
smaller with large enough N and b -- and since we are talking about storing data
to disk for use in databases, etc., the amount of data is usually large enough
to justify this.

### What do you understand by Distributed Transaction?

**Distributed Transaction** is any situation where a single event results in the
mutation of two or more separate sources of data which cannot be committed
automatically. In the world of microservices, it becomes even more complex as
each service is a unit of work and most of the time multiple services have to
work together to make a business successful.
