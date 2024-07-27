## Basic NestJS Interview Questions and Answers

#### Table of Contents

- [What is NestJS?](#what-is-nestjs)
- [What are some features of NestJS?](#what-are-some-features-of-nestjs)
- [Is it possible to use any other language with NestJS?](#is-it-possible-to-use-any-other-language-with-nestjs)
- [What are the main components of NestJS?](#what-are-the-main-components-of-nestjs)
- [What is the responsibility of a controller?](#what-is-the-responsibility-of-a-controller)
- [What is the responsibility of a module?](#what-is-the-responsibility-of-a-module)
- [What is the responsibility of a service?](#what-is-the-responsibility-of-a-service)
- [What is the use of middleware in NestJS?](#what-is-the-use-of-middleware-in-nestjs)
- [In each module, we have controller files with extension as spec.ts, what is this file used for?](#in-each-module-we-have-controller-files-with-extension-as-spects-what-is-this-file-used-for)
- [What is the entry file of NestJs application?](#what-is-the-entry-file-of-nestjs-application)
- [What are the two supported platforms by NestJs?](#what-are-the-two-supported-platforms-by-nestjs)

### What is NestJS?

Nest (NestJS) is a Node.js framework for building efficient and scalable
server-side applications. It was developed by Kamil Mysliwiec and built on the
top of Express and Typescript.

### What are some features of NestJS?

Support for multiple DataBases, use of Typescript (less error prone app) and
main feature that NestJS gives is it's Modular Structure.

### Is it possible to use any other language with NestJS?

Yes, it can work with any language that can compile to JavaScript. You only need
a perfect Compiler that can compile code to Javascript so that JS engine can
understand it.

### What are the main components of NestJS?

The main components of a NestJS application are the controller, service, and
module.

### What is the responsibility of a controller?

A Controller's purpose is responsible for handling incoming requests and sending
response to the client.

### What is the responsibility of a module?

The module is responsible for organizing the application. A NestJS application
has at least one Root Module which is the starting point that NestJs uses to
build application Graph.

### What is the responsibility of a service?

Services are used in NestJS to write business logic.

### What is the use of middleware in NestJS?

In NestJs, Middlewares are functions that are executed before any route handler.

- Client (Http Request) -> Middlewares -> Route Handler which means that each
  request will be first served by Middleware and if it meets the specific
  criteria then only it'll be executed by route handler.

### In each module, we have controller files with extension as spec.ts, what is this file used for?

These are used for Unit Testing.

### What is the entry file of NestJs application?

main.ts is the file which uses the core NestFactory class to create a Nest
application instance.

### What are the two supported platforms by NestJs?

1. platform-express (a.k.a NestExpressApplication) which is used by default as
   `@nestjs/platform-express` package

2. platform-fastify (a.k.a NestFastifyApplication)

#### [Content Source](https://www.shanumittal.com/blogs/technology/nestjs-interview-questions-answers)
