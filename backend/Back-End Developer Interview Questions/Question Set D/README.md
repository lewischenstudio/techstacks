## Question Set D

#### Table of Contents

- [What is GOD class and why should we avoid it?](#what-is-god-class-and-why-should-we-avoid-it)
- [What is Spike Testing?](#what-is-spike-testing)
- [What is BASE property of a system?](#what-is-base-property-of-a-system)
- [What's the difference between _Faking_, _Mocking_, and _Stubbing_?](#whats-the-difference-between-faking-mocking-and-stubbing)
- [What's the difference between principles YAGNI and KISS?](#whats-the-difference-between-principles-yagni-and-kiss)
- [When to use Redis or MongoDB?](#when-to-use-redis-or-mongodb)
- [Why layering your application is important? Provide some bad layering example](#why-layering-your-application-is-important-provide-some-bad-layering-example)
- [Are you familiar with the Twelve-Factor App principles?](#are-you-familiar-with-the-twelve-factor-app-principles)
- [How would you implement SSO for Microservie Architecture?](#how-would-you-implement-sso-for-microservie-architecture)
- [Name some best practices for better RESTful API design](#name-some-best-practices-for-better-restful-api-design)

### What is GOD class and why should we avoid it?

A **GOD** class -- or, alternatively, god object -- is an anti-pattern that
consists of having a class that does too much. A god class is usually a huge
class that concentrates a lot of responsibilities, controls and oversees many
different objects, and effectively does everything in the application. One code
change will most likely affect other parts of the class and therefore indirectly
all other classes that use it. That in turn leads to an even bigger maintenance
mess since no one dares to do any changes other than adding new functionality to
it.

### What is Spike Testing?

**Spike Testing** is a type of stress testing that evaluates software
performance when workloads are substaintially increased quickly and repeatedly.
The workload is beyond normal expectations for short amounts of time.

### What is BASE property of a system?

_BASE_ properties are the common properties of recently evolved NoSQL databases.
According to CAP theorm, a BASE system does not guarantee consistency. This is a
contrived acronym that is mapped to following property of a system in terms of
the CAP theorm.

- **Basically Availability** indicates that the system is guaranteed to be
  available.
- **Soft-state** indicates that the state of the system may change over time,
  even without input. This is mainly due to the eventually consistent model.
- **Eventual Consistency** indicates that the system will become consistent over
  time, given that the system doesn't receive input during that time.

### What's the difference between _Faking_, _Mocking_, and _Stubbing_?

- **Fake** objects actually have working implementations, but usually take some
  shortcut which makes them not suitable for production.
- **Stubs** provide canned answers to calls made during the test, usually not
  responding at all to anything outside what's programmed in for the test. Stubs
  may also record information about calls, such as email gateway stub that
  remembers the messages it "sent", or maybe only how many messages it "sent".
- **Mocks** are what we are talking about here: object pre-programmed with
  expectations which form a specification of the calls they are expected to
  receive.

### What's the difference between principles YAGNI and KISS?

- **YAGNI (You aint gonna need it)** refers to over analyzing and implementing
  things that may or may not be needed. Sure algorithmic elegance is nice and
  all but most situation you don't need it. In general engineering terms you
  shouldbe careful not to include your own requirements so that you don't taint
  your customer needs with your own idea that end up costing the project with
  little impact for the client.
- **KISS (Keep it simple stupid)** refers to the fact that easy systems are
  easier to manage. Keeping things simple is not necessarily less work (like
  YAGNI is) since it requires more knowledge to implement. They are sometimes
  similar but grow from different needs.

YAGNI grows from too much future anticipation, overzealous workers if you may.
KISS is a strategy that tries to counteract human tendency for design creep.

### When to use Redis or MongoDB?

- **Use MongoDB if you don't know yet how you're going to query your data or
  what schema to stick with**. MongoDB is suited for Hackathons, startups or
  every time you don't know how you'll query the data you inserted. MongoDB does
  not make any assumptions on your underlying schema. While MongoDB is
  schemaless and non-relational, this does not mean that there is no schema at
  all. It simply means that your schema needs to be defined in your app (e.g.
  using Mongoose). Besides that, MongoDB is great for prototyping or trying
  things out. Its performance is not that great and can't be compared to Redis.
- **Use Redis in order to speed up your existing application**. It is very
  uncommon to use Redis as a standalone database system (some people prefer
  referrring to it as a "key-value"-store).

### Why layering your application is important? Provide some bad layering example.

Each component should contain "layers" -- a dedicated object for the web, logic
and data access code. This not only draws a clean _separation of concerns_ but
also significantly eases mocking and testing the system.

Though this is a very common pattern, API developers tend to mix layers by
passing the web layer objects (for example Express req, ers) to business logic
and data layers -- this makes your application dependent on and accessible by
Express only. App that mixes objects with other layers cannot be accessed by
testing code. CRON jobs and other non-Express callers.

### Are you familiar with the Twelve-Factor App principles?

The **Twelve-Factor** app is an excellent security pattern designed to
dramatically improve the security of any website or mobile app that users log
into, making them almost completely impenetrable. The idea behind the
twelve-factor app is that when a user logs into a websites, then the mobile app
with this account becomes insecure.

Once developers began realizing that username/password login was insecure, they
started experimenting with multiple factors. The way two-factor authentication
worked was a little more complicated, but far more secure:

- A user would visit a login page and enter their username/password just like
  before
- If the username/password entered were valid, then the user would receive an
  SMS message containing a number
- If the user would then be required to enter that number into the website to
  _prove_ that they had access to their cell phone, and that user was therefore
  who they claimed to be

The twelve-factor app is a new best practice for building secure login systems
that picks up where multi-factor left off.

Instead of allowing a user to configure different factors they can choose from
to log in — a twelve-factor compliant app requires each user to have twelve
different authentication factors and to use them each time they log into a
website or mobile app.

Here’s an example of a twelve-factor compliant app:

A user visits a website and enters their username/password (factor 1)

- The user then receives an SMS message and types in a code
- The user then opens their Google Authenticator app on their phone and enters
  the code from there
- The user then opens their Authy app on their phone and enters the code from
  there
- The user then opens their Okta Verify app on their phone and enters the code
  from there
- The user then uses FaceID to have their face detected
- The user then presses their finger up against the fingerprint scanner on their
  phone and uses that to confirm their fingerprint
- The user then says their “voice password” out loud when their phone prompts
  them (this does voice recognition)
- The user then enters their preferred credit card number into the app when
  requested to confirm that their billing - details are known
- The user then enters their social security number which helps verify their
  identity
- The user then enters their birthday
- Finally, the user enters private genome data about themselves that is
  cross-referenced against the 23andMe API.

While this process is slightly inconvenient for a user to repeat each time they
log in, in provides superior protection against attackers and makes you
virtually hacker-proof.

### How would you implement SSO for Microservie Architecture?

For microservices taht must connect to other microservices or to external
services demanding access through API, SSO (Single sign-on) can also be enabled.
In this case, a software entity or service account -- not actual users -- needs
to be authorized. The same IAM solution is available. The IAM system may be
contacted when a software entity needs access, and it will then provide them
with an SSO token to utilize for further API requests.

### Name some best practices for better RESTful API design

- REST API must accept and respond with JSON
- Go with error status codes
- Don't use verbs in URLs
- Use plural nouns to name a collection
- Well compiled documentation
- Return error details in the response body
- Use resource nesting
- Use SSL/TLS
- Secure your API
