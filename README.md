# Full-stack Developer Interview Questions and Answers

## <a name='toc'>Table of Contents</a>

  1. [General Questions](#general)
  1. [Architecture](#architecture)
  1. [WEB](#web)
  1. [SQL](#sql)
  1. [NoSQL](#nosql)
  1. [Transactions](#transcations)
  1. [Scalability](#scalability)
  1. [Load balancing](#load-balancing)
  1. [Cloud computing](#cloud-computing)
  1. [Distributed](#distributed)
  1. [Cache](#cache)
  1. [Concurrency](#concurrency)
  1. [Networking](#networking)
  1. [Operating system](#os)
  1. [Compilers](#compilers)
  1. [Java](#java)
  1. [Javascript](#javascript)
  1. [Python](#python)
  1. [C++](#cpp)
  1. [Code writing](#codewriting)
  1. [Functional programming](#functional-programming)
  1. [Reactive programming](#reactive-programming)
  1. [Git](#git)
  1. [DevOps](#devOps)
  1. [QA](#qa)
  1. [Agile, Scrum, XP](#agile)
  1. [Algorithms](#algorithms)
  1. [UML](#uml)
  1. [Other](#other)
  1. [Machine learning](#machine-learning)
  1. [Big Data](#big-data)
  1. [Image processing](#image-processing)
  1. [Cryptography](#cryptography)
  1. [Security](#security)
  1. [Android](#android)
  1. [Books](#books)

#### [[⬆]](#toc) <a name='general'>General Questions:</a>
* [*Polymorphism*](https://en.wikipedia.org/wiki/Polymorphism_(computer_science)) (Variable of type Shape could refer to an object of type Square, Circle... Ability of a function to handle objects of many types)
* [*Encapsulation*](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)) (Packing of data and functions into a single component)
* [*Virtual function*](https://en.wikipedia.org/wiki/Virtual_function) (Overridable function)
* [*Virtual method table*](https://en.wikipedia.org/wiki/Virtual_method_table)
* [*Dynamic binding*](https://en.wikipedia.org/wiki/Late_binding) (Actual method implementation invoked is determined at run time based on the class of the object, not the type of the variable or expression)
* How does [*garbage collector*](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science)) work? (Mark and sweep: mark: traverse object graph starting from root objects, sweep: garbage collect unmarked objects. Optimizations: young/old generations, incremental mark and sweep)
* [*Tail recursion*](https://en.wikipedia.org/wiki/Tail_call) (A tail call is a subroutine call performed as the final action of a procedure)
* [*Semantic versioning*](http://semver.org)

#### [[⬆]](#toc) <a name='architecture'>Architecture:</a>
* *Design principles*. ([*SOLID*](https://en.wikipedia.org/wiki/SOLID_(object-oriented_design)), [*DRY*](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself), [*KISS*](https://en.wikipedia.org/wiki/KISS_principle), [*YAGNI*](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it), [*Occam's razor*](https://en.wikipedia.org/wiki/Occam%27s_razor), [*Worse is better*](https://en.wikipedia.org/wiki/Worse_is_better), [*convention over configuration*](https://en.wikipedia.org/wiki/Convention_over_configuration), [*separation of concerns*](https://en.wikipedia.org/wiki/Separation_of_concerns), [*Law of Demeter (principle of least knowledge)*](https://en.wikipedia.org/wiki/Law_of_Demeter), boy scout rule, [*single source of truth*](https://en.wikipedia.org/wiki/Single_source_of_truth), [*single version of truth*](https://en.wikipedia.org/wiki/Single_version_of_the_truth), [*principle of least astonishment*](https://en.wikipedia.org/wiki/Principle_of_least_astonishment), [*let it crash principle*](https://en.wikipedia.org/wiki/Crash-only_software), [*inversion of control*](https://en.wikipedia.org/wiki/Inversion_of_control))
* [*SOLID*](https://en.wikipedia.org/wiki/SOLID_(object-oriented_design))

|Rule|Description|
|:--|:--|
|[**S**ingle responsibility principle](https://en.wikipedia.org/wiki/Single_responsibility_principle)|A module should be responsible to one, and only one, actor.|
|[**O**pen/closed principle](https://en.wikipedia.org/wiki/Open/closed_principle)|A software artifact should be open for extension but closed for modification.|
|[**L**iskov substitution principle](https://en.wikipedia.org/wiki/Liskov_substitution_principle)|It should be possible to substitute the derived class with base class.|
|[**I**nterface segregation principle](https://en.wikipedia.org/wiki/Interface_segregation_principle)|Many client-specific interfaces are better than one general-purpose interface.|
|[**D**ependency inversion principle](https://en.wikipedia.org/wiki/Dependency_inversion_principle)|Depend upon Abstractions but not on concretions. This means that each module should be separated from other using an abstract layer which binds them together. Source code dependency points in the opposite direction compared to the flow of control.|

* [*The Clean Architecture*](https://8thlight.com/blog/uncle-bob/2012/08/13/the-clean-architecture.html)
* [*Clean Code Cheat Sheet*](https://www.planetgeek.ch/wp-content/uploads/2014/11/Clean-Code-V2.4.pdf)
* [*One key abstraction*](http://wiki3.cosc.canterbury.ac.nz/index.php/One_key_abstraction)
* [*Aspect-oriented programming*](https://en.wikipedia.org/wiki/Aspect-oriented_programming)
* [*The Twelve-Factor App*](http://12factor.net)
* [*Domain-driven design*](https://en.wikipedia.org/wiki/Domain-driven_design)
* [*Microservices*](https://en.wikipedia.org/wiki/Microservices) are a style of software architecture that involves delivering systems as a set of very small, granular, independent collaborating services. 
* Pros of *microservices* (The services are easy to replace, Services can be implemented using different programming languages, databases, hardware and software environment, depending on what fits best)
* *Design patterns*. (**Creational**: [*Builder*](https://refactoring.guru/design-patterns/builder), [*Object Pool*](https://en.wikipedia.org/wiki/Object_pool_pattern), [*Factory Method*](https://refactoring.guru/design-patterns/factory-method), [*Signleton*](https://refactoring.guru/design-patterns/singleton), [*Multiton*](https://en.wikipedia.org/wiki/Multiton_pattern), [*Prototype*](https://refactoring.guru/design-patterns/prototype), [*Abstract Factory*](https://refactoring.guru/design-patterns/abstract-factory). **Structural**: [*Adapter*](https://refactoring.guru/design-patterns/adapter), [*Bridge*](https://refactoring.guru/design-patterns/bridge), [*Composite*](https://refactoring.guru/design-patterns/composite), [*Decorator*](https://refactoring.guru/design-patterns/decorator), [*Facade*](https://refactoring.guru/design-patterns/facade), [*Flyweight*](https://refactoring.guru/design-patterns/flyweight), [*Proxy*](https://refactoring.guru/design-patterns/proxy). **Behavioral**: [*Chain of Responsibility*](https://refactoring.guru/design-patterns/chain-of-responsibility), [*Command*](https://refactoring.guru/design-patterns/command), [*Interpreter*](https://en.wikipedia.org/wiki/Interpreter_pattern), [*Iterator*](https://refactoring.guru/design-patterns/iterator), [*Mediator*](https://refactoring.guru/design-patterns/mediator), [*Memento*](https://refactoring.guru/design-patterns/memento), [*Observer*](https://refactoring.guru/design-patterns/observer), [*State*](https://refactoring.guru/design-patterns/state), [*Strategy*](https://refactoring.guru/design-patterns/strategy), [*Template Method*](https://refactoring.guru/design-patterns/template-method), [*Visitor*](https://refactoring.guru/design-patterns/visitor).)
* [*Enterprise integration patterns*](https://en.wikipedia.org/wiki/Enterprise_Integration_Patterns), [*SOA patterns*](www.soapatterns.org).
* [*3-tier architecture*](https://en.wikipedia.org/wiki/Multitier_architecture) (Presentation tier, Application tier, Data tier)
* *3-layer architecture* (DAO (Repository), Business (Service) layer, Controller)
* [*REST*](https://en.wikipedia.org/wiki/Representational_state_transfer) (Representational state transfer), [*RPC*](https://en.wikipedia.org/wiki/Remote_procedure_call)
* [*Idempotent operation*](https://en.wikipedia.org/wiki/Idempotence) (The PUT and DELETE methods are referred to as idempotent, meaning that the operation will produce the same result no matter how many times it is repeated)
* *Nullipotent operation* (GET method is a safe method (or nullipotent), meaning that calling it produces no side-effects)
* [*Naked objects*](https://en.wikipedia.org/wiki/Naked_objects), [*Restful objects*](https://en.wikipedia.org/wiki/Restful_Objects).
* Why do you need *web server* (tomcat, jetty)?
* [*Inheritance*](https://en.wikipedia.org/wiki/Inheritance_(object-oriented_programming)) vs [*Composition*](https://en.wikipedia.org/wiki/Object_composition) (Inheritance - is-a relationship, whether clients will want to use the subclass type as a superclass type. Composition - has-a or part-of relationship).
* [*Multiple inheritance (diamond) problem*](https://en.wikipedia.org/wiki/Multiple_inheritance#The_diamond_problem)
* Advantages of using *modules*. (reuse, decoupling, namespace)
* Drawbacks of not using [*separation of concerns*](https://en.wikipedia.org/wiki/Separation_of_concerns)
  * Adding new features will take an order of magnitude longer
  * Impossible to optimize
  * Extremely difficult to test
  * Fixing and debugging can be a nightmare (fixing something in one place can lead to something else breaking that seems completely unrelated).
* What is [*uniform access principle*](https://en.wikipedia.org/wiki/Uniform_access_principle)? (client code should not be affected by a decision to implement an attribute as a field or method)
* [Conway's law](https://en.wikipedia.org/wiki/Conway%27s_law) (organizations which design systems ... are constrained to produce designs which are copies of the communication structures of these organizations)
* [GRASP](https://en.wikipedia.org/wiki/GRASP_(object-oriented_design))

#### [[⬆]](#toc) <a name='web'>WEB:</a>
* WEB security vulnerabilities ([*XSS*](https://en.wikipedia.org/wiki/Cross-site_scripting), [*CSRF*](https://en.wikipedia.org/wiki/Cross-site_request_forgery), [*session fixation*](https://en.wikipedia.org/wiki/Session_fixation), [*SQL injection*](https://en.wikipedia.org/wiki/SQL_injection), [*man-in-the-middle*](https://en.wikipedia.org/wiki/Man-in-the-middle_attack), [*buffer overflow*](https://en.wikipedia.org/wiki/Buffer_overflow))
* *CSRF prevention* (CSRF-token)
* What is [*JSONP*](https://en.wikipedia.org/wiki/JSONP), [*CORS*](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing)? (A communication technique used in JavaScript programs running in web browsers to request data from a server in a different domain, something prohibited by typical web browsers because of the same-origin policy)
* HTTPS negotiation steps.
* What is HTTP Strict Transport Security ([*HSTS*](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security))? (Prevents Man in the Middle attacks)
* Browser-server communication methods: WebSocket, EventSource, Comet(Polling, Long-Polling, Streaming)
* [*Character encoding*](https://en.wikipedia.org/wiki/Character_encoding)
* What is *role-based access control* and *access control list*?
* What is session and persistent cookies, sessionStorage and localStorage?
* How to implement *remember-me*? (http://jaspan.com/improved_persistent_login_cookie_best_practice)
* Authentication using cookies, [*JWT*](https://en.wikipedia.org/wiki/JSON_Web_Token) (JSON Web Tokens).
* How *OAuth 2.0* works?

#### [[⬆]](#toc) <a name='sql'>SQL:</a>
* *SQL join types* (inner join, left/right outer join, full outer join, cross join)
![Join types](https://habrastorage.org/files/7ff/b2c/3a2/7ffb2c3a25b74dcf9eec013282b9cfb4.png "Join types"))
* *SQL normal forms* (1.The domain of each attribute contains only atomic values, and the value of each attribute contains only a single value from that domain. 2.No non-prime attribute in the table is functionally dependent on a proper subset of any candidate key. 3.Every non-prime attribute is non-transitively dependent on every candidate key in the table. BCNF.Every non-trivial functional dependency in the table is a dependency on a superkey.)
* *Isolation levels* and Anomalies (Read Uncommitted, Read Committed, Repeatable Read, Serializable

|Isolation_level\Anomaly|Lost_update (because of rollback)|Dirty_read|Non_repeatable_reads second_lost_update|Phantoms|Write_skew|
|:---------------|:-------:|:-------:|:-------:|:-------:|:-------:|
|Read Uncommitted|-        |may occur|may occur|may occur|may occur|
|Read Committed  |-        |-        |may occur|may occur|may occur|
|Repeatable Read |-        |-        |-        |may occur|may occur|
|Snapshot        |-        |-        |-        |-        |may occur|
|Serializable    |-        |-        |-        |-        |-        |

#### [[⬆]](#toc) <a name='nosql'>NoSQL:</a>
* Types of NoSQL databases?
  * Document Stores (MongoDB, Couchbase)
  * Key-Value Stores (Redis, Volgemort)
  * Column Stores (Cassandra)
  * Graph Stores (Neo4j, Giraph)

#### [[⬆]](#toc) <a name='transactions'>Transactions:</a>
* [*ACID*](https://en.wikipedia.org/wiki/ACID)
* [*2-phase commit protocol*](https://en.wikipedia.org/wiki/Two-phase_commit_protocol)
* [*3-phase commit protocol*](https://en.wikipedia.org/wiki/Three-phase_commit_protocol)
* What is *pessimistic*/[*optimistic*](https://en.wikipedia.org/wiki/Optimistic_concurrency_control) locking?

#### [[⬆]](#toc) <a name='scalability'>Scalability:</a>
* Horizontal and vertical scaling.
* How to scale database? (Data partitioning, sharding(vertical/horizontal), replication(master-slave, master-master)).
* *Denormalization*.
* What is *synchronous multimaster replication*? (Each server can accept write requests, and modified data is transmitted from the original server to every other server before each transaction commits)
* What is *asynchronous multimaster replication*? (Each server works independently, and periodically communicates with the other servers to identify conflicting transactions. The conflicts can be resolved by users or conflict resolution rules)
* When to use messaging queue?
* MongoDB, Redis.
* Hadoop basics.

#### [[⬆]](#toc) <a name='load-balancing'>Load balancing:</a>
* sticky/non-sticky sessions
* *Sticky sessions* vs storing sessions in Redis.

#### [[⬆]](#toc) <a name='cloud-computing'>Cloud computing:</a>
* What is *cloud computing*? (Cloud computing platform is a fully automated server platform that allows users to purchase, remotely create, dynamically scale, and administer system)
* *Amazon web services*

#### [[⬆]](#toc) <a name='distributed'>Distributed:</a>
* [*Consensus*](https://en.wikipedia.org/wiki/Consensus_(computer_science))
* [*Raft*](https://en.wikipedia.org/wiki/Raft_(computer_science)) ([In Search of an Understandable Consensus Algorithm](https://raft.github.io/raft.pdf))
* [*Paxos*](https://en.wikipedia.org/wiki/Paxos_(computer_science))
* What is *CAP theorem*? (It is impossible for a distributed computer system to simultaneously provide all three of the following guarantees: *consistency*, *availability*, *partition tolerance*). ["Please stop calling databases CP or AP"](https://martin.kleppmann.com/2015/05/11/please-stop-calling-databases-cp-or-ap.html))
![CAP theorem](http://guide.couchdb.org/draft/consistency/01.png "CAP theorem")
* What is *map-reduce*? (Word count example)
* *Sharding counters*.
* Distributed software:
  * Distributed streaming platforms: **kafka**
  * Distributed key-value store: **zookeeper**, **etcd**, **Consul**
  * Map-reduce: **hadoop**, **spark**
  * Distributed file system: **hbase**
  * Cluster management: **kubernetes**, **docker-swarm**, **mesos**
* Herlihy’s consensus hierarchy. Every shared object can be assigned a consensus number, which is the maximum number of processes for which the object can solve wait-free consensus in an asynchronous system.
```
1 Read-write registers
2 Test-and-set, swap, fetch-and-add, queue, stack
⋮ ⋮
∞ Augmented queue, compare-and-swap, sticky byte
```
* *Consensus number*. Maximum number of threads for which objects of the class can solve consensus problem.

#### [[⬆]](#toc) <a name='cache'>Cache:</a>
* What is *write-through* and *write-behind* caching? (write-through (synchronous), write-behind (asynchronous))
* HTTP cache options?

#### [[⬆]](#toc) <a name='concurrency'>Concurrency:</a>
* What is *deadlock*, *livelock*? (Deadlock is a situation in which two or more competing actions are each waiting for the other to finish, and thus neither ever does. A livelock is similar to a deadlock, except that the states of the processes involved in the livelock constantly change with regard to one another, none progressing.)
* Deadlock avoidance. (prevention, detection, avoidance (Mutex hierarchy), and recovery)
* What is *starvation*? ()
* What is *race condition*? (Behavior of software system where the output is dependent on the sequence or timing of other uncontrollable events)
* What is *happens-before* relation?
* What is *thread contention*? (Contention is simply when two threads try to access either the same resource or related resources in such a way that at least one of the contending threads runs more slowly than it would if the other thread(s) were not running). Contention occurs when multiple threads try to acquire a lock at the same time
* What is a *thread-safe function*? (Can be safely invoked by multiple threads at the same time)
* Publish/Subscripe code
* What is *2-phase locking*? (Growing phase, shrinking phase. Guarantees serializablity for transactions, doesn't prevent deadlock).
* What is the difference between *thread* and *process*? (Threads (of the same process) run in a shared memory space, while processes run in separate memory spaces)
* What is *false sharing*, *cache pollution*, *cache miss*, *thread affinity*, *speculative execution*, *ABA-problem*?
* What is *lock-free* and *wait-free* algorithm?
* What is *sequential consistency*? (The result of any execution is the same as if the operations of all the processors were executed in some sequential order, and the operations of each individual processor appear in this sequence in the order specified by its program).
* What is *memory barrier*? (A memory barrier, also known as a membar, memory fence or fence instruction, is a type of barrier instruction that causes a CPU or compiler to enforce an ordering constraint on memory operations issued before and after the barrier instruction)
* Synchonization aids in Java
  * CountDownLatch
  * CyclicBarrier
  * Phaser
  * ReentrantLock
  * Exchanger
  * Semaphore
  * LinkedTransferQueue
* What is *data race*? (When a program contains two conflicting accesses that are not ordered by a happens-before relationship, it is said to contain a data race. Two accesses to (reads of or writes to) the same variable are said to be conflicting if at least one of the accesses is a write)
* Java *memory model*. (A program is correctly synchronized if and only if all sequentially consistent executions are free of data races. Correctly synchronized programs have sequentially consistent semantics. Causality requirement for incorrectly synchronized programs. [link](https://pdfs.semanticscholar.org/c132/11697f5c803221533a07bd6db839fa60b7b8.pdf))
* What is *monitor* in Java? (Each object in Java is associated with a monitor, which a thread can lock or unlock)
* What is *safe publication*?
* What is *wait*/*notify*?
* *Amdahl's law*? (Speedup = 1 / (1 - p + p / n))
* *Dining philosophers problem* (Resource hierarchy (first take lower-indexed fork), arbitrator, communication (dirty/clean forks)).
* *Produces/consumer* problem.
* *Readers/writers* problem.
* [*Transactional memory*](https://en.wikipedia.org/wiki/Software_transactional_memory)
* [Coroutine](https://en.wikipedia.org/wiki/Coroutine)

#### [[⬆]](#toc) <a name='networking'>Networking:</a>
* OSI model (Physical, Data link, Network, Transport, Session, Presentation, Application)
* Multithreading vs select
* [*Switch*](https://en.wikipedia.org/wiki/Network_switch), [*hub*](https://en.wikipedia.org/wiki/Ethernet_hub), [*router*](https://en.wikipedia.org/wiki/Router_(computing))
* [*TCP congestion*](https://en.wikipedia.org/wiki/TCP_congestion_control)
* *TCP back-pressure*

#### [[⬆]](#toc) <a name='os'>Operating system:</a>
* What is [*memory mapped*](https://en.wikipedia.org/wiki/Memory-mapped_file) file and its benefits?
* *Interprocess communication* methods. (Pipes, Events, Mailboxes/Ports (can be implemented by using shared memory and semaphores), Direct Message Passing).
* [*Virtual memory*](https://en.wikipedia.org/wiki/Virtual_memory) organization.
* *Process scheduler*.

#### [[⬆]](#toc) <a name='compilers'>Compilers:</a>
* [*Recursive descent parser*](https://en.wikipedia.org/wiki/Recursive_descent_parser)
* [*LL parser*](https://en.wikipedia.org/wiki/LL_parser)
* [*LR parser*](https://en.wikipedia.org/wiki/LR_parser)
* [*Context-free grammar*](https://en.wikipedia.org/wiki/Context-free_grammar)
* [*Chomsky hierarchy*](https://en.wikipedia.org/wiki/Chomsky_hierarchy)

#### [[⬆]](#toc) <a name='java'>Java:</a>
* [*PhantomReference*](https://en.wikipedia.org/wiki/Phantom_reference), [*WeakReference*](https://en.wikipedia.org/wiki/Weak_reference), [*SoftReference*](https://en.wikipedia.org/wiki/Soft_reference), *finalize()*, *ReferenceQueue*.
* How to correctly stop a thread? (Thread.interrupt())
* What is *Spring*? (Spring Framework is an application container for Java that supplies many useful features, such as Inversion of Control, Dependency Injection, abstract data access, transaction management, and more)
  * Spring is a framework for dependency injection: a design pattern that allows the developer to build very decoupled systems by injecting dependencies into classes.
  * It elegantly wraps Java libraries and makes then much easier to use in your application.
  * Included in the framework are implementations of commonly used patterns such as REST and MVC web framework which are predominately use by in web applications.
* What is *Spring-Boot*?
* What is *Hibernate* and JPA (Caches, lazy-loading)?
* *Garbage collection*. (G1, Young/Old generation collectors combination examples: PS Scavenge/PS MarkSweep, Copy/MarkSweepCompact)
* How to write *benchmarks*? ([jmh](http://openjdk.java.net/projects/code-tools/jmh/))
* What are Java 9 modularity?
* What is OSGI? (Specification describes a modular system and a service platform for the Java programming language that implements a complete and dynamic component model. Each bundle has its own classpath. Dependency hell avoidance. META-INF/MANIFEST.MF contains OSGI-info)
* Serializable / Externalizable
* What is a *servlet* (versions of servlet api, Servlet 4.0)?
* What is a *servlet filter*? How to implement *GZipFilter*? (ResponseWrapper)
* What is *generics* and PECS (producer extends and consumer super)?
* What is the difference between <?>, \<Object\>, <? extends Object> and no generic type? [link1](http://stackoverflow.com/questions/8055389/whats-the-difference-between-and-extends-object-in-java-generics) [link2](http://stackoverflow.com/questions/678822/what-is-the-difference-between-and-object-in-java-generics)
* Explain method signature for [Collections.max(...)](https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html#max-java.util.Collection-), [Collections.fill(...)](https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html#fill-java.util.List-T-), [Collections.copy(...)](https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html#copy-java.util.List-java.util.List-), [Collections.sort(...)](https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html#sort-java.util.List-java.util.Comparator-)
* Why are arrays covariant but generics are invariant? [link](http://stackoverflow.com/questions/18666710/why-are-arrays-covariant-but-generics-are-invariant)
* Major specs: JAX-RS, JAX-WS, JMS, JAXB, XSLT, XPATH, JNDI, JMX, JDBC, XML(SAX, DOM, StAX)

#### [[⬆]](#toc) <a name='javascript'>Javascript:</a>
* this keyword
* How *prototypes* work?
* inheritance
* differences between == and === (http://dorey.github.io/JavaScript-Equality-Table/)
* closures
* recursion 
* What is *MVC*, *MVP*, *MVVM*?
* What is *promise*?
* What is event *bubbling* and *capturing*? (target.addEventListener(type, listener[, useCapture]))
* What is *AMD*(Asynchronous Module Design) and *CommonJS*?
* What is *jQuery*?

#### [[⬆]](#toc) <a name='codewriting'>Codewriting:</a>
* Implement binary search
```java
int binarySearch(int[] a, int fromInclusive, int toExclusive, int key) {
    int low = fromInclusive;
    int high = toExclusive - 1;
    while (low <= high) {
        int mid = (low + high) >>> 1;
        int midVal = a[mid];
        if (midVal < key)
            low = mid + 1;
        else if (midVal > key)
            high = mid - 1;
        else
            return mid; // key found
    }
    return -(low + 1); // key not found
}
```
* Implement quick sort
```java
void qSort(int[] a, int fromInclusive, int toInclusive) {
    int i = fromInclusive;
    int j = toInclusive;
    if (i >= j) return;
    int separator = a[i + random.nextInt(j - i + 1)];
    do {
        while (a[i] < separator) ++i;
        while (a[j] > separator) --j;
        if (i > j) break;
        int t = a[i];
        a[i] = a[j];
        a[j] = t;
        ++i;
        --j;
    } while (i <= j);
    qSort(a, fromInclusive, j);
    qSort(a, i, toInclusive);
}
```

#### [[⬆]](#toc) <a name='functional-programming'>Functional programming:</a>
* [*Referential transparency*](https://en.wikipedia.org/wiki/Referential_transparency)
* What is [*Monad*](https://en.wikipedia.org/wiki/Monad_(functional_programming))?

#### [[⬆]](#toc) <a name='reactive-programming'>Reactive programming:</a>
* [*The Reactive Manifesto*](http://www.reactivemanifesto.org) (responsive, resilient, elastic, message driven)
* What is *asynchronous* and *non-blocking*? [link](https://www.linkedin.com/pulse/java-servlets-asynchronous-non-blocking-aliaksandr-liakh)

#### [[⬆]](#toc) <a name='git'>Git:</a>
* *Git* workflow? (Master: production-ready state; Develop: latest delivered development changes for the next release; Feature Branches; Release Branches; Hotfixes) ![Git workflow](http://nvie.com/img/git-model@2x.png "Git workflow") http://nvie.com/posts/a-successful-git-branching-model/
* What is a rebase?

#### [[⬆]](#toc) <a name='devOps'>DevOps:</a>
* What is *Blue-green Deployment*, *Canary release*, *A/B testing*? [link](https://www.javacodegeeks.com/2016/02/blue-green-deployment.html)
* What is *Docker*?

#### [[⬆]](#toc) <a name='qa'>QA:</a>
* What is *unit test*? (A test that purely tests a single unit of functionality)
* What is *component test*?
* What is *integration test*? (Examine several parts of a system to make sure that when integrated, these parts behave as expected)
* What is *user acceptance test*? BDD?
* Unit tests advantages?
* Types of tests: acceptance testing, functional testing, smoke testing, regression testing, unit testing, integration testing, stress testing, (Load, Performance, Sanity, Stability, Security, Feature, Progression, Installation, Business).
* Differences between stub and mock? (A stub is a test double with preprogrammed behavior. Mocks are stubs with preprogrammed expectations)
* Selenium tests and webdriver.
* How to test multithreading code?
* What is *Consumer Driven Contract*? [link](https://cloud.spring.io/spring-cloud-contract/spring-cloud-contract.html)

#### [[⬆]](#toc) <a name='agile'>Agile:</a>
* What is Agile? (http://agilemanifesto.org/principles.html)
  * Individuals and interactions over Processes and tools
  * Working software over Comprehensive documentation
  * Customer collaboration over Contract negotiation
  * Responding to change over Following a plan
* What is Scrum? (Roles: product owner, development team, scrum master. Events: sprint)
* What are the differences between Scrum and Waterfall? ( http://www.leanagiletraining.com/agile/waterfall-versus-scrum-how-do-they-compare/)
* What is XP? ()
* What is Kanban?
* What is Lean development?

#### [[⬆]](#toc) <a name='algorithms'>Algorithms:</a>
* What Ο(n), Ω(n), Θ(n)?
* What is NP, NP-completeness, NP-hardness with examples?

#### [[⬆]](#toc) <a name='other'>Other:</a>
* How to find memory leak. (Memory snapshot diff).
* Profiling: sampling and instrumentation.
* Regular expressions. (Examples)
* What are your goals to work in our company? (3 categories: professional, financial, social)
* What is *virtualization*?
* What is total/partial order?
* How to work with legacy code? (http://programmers.stackexchange.com/a/122024)

#### [[⬆]](#toc) <a name='machine-learning'>Machine learning:</a>
* [*Confidence interval*](https://en.wikipedia.org/wiki/Confidence_interval)
* [*p-value*](https://en.wikipedia.org/wiki/P-value)
* [*Overfitting*](https://en.wikipedia.org/wiki/Overfitting)
* [*Bias–variance tradeoff*](https://en.wikipedia.org/wiki/Bias–variance_tradeoff)
* [*Bayes' theorem*](https://en.wikipedia.org/wiki/Bayes%27_theorem) P(A|B) = P(B|A)P(A)/P(B), P(B) = sum(P(Ai)P(B|Ai))

#### [[⬆]](#toc) <a name='big-data'>Big Data:</a>
* [*Lambda architecture*](https://en.wikipedia.org/wiki/Lambda_architecture)
* [*HyperLogLog*](https://en.wikipedia.org/wiki/HyperLogLog)
* [*Event sourcing*](http://microservices.io/patterns/data/event-sourcing.html)

#### [[⬆]](#toc) <a name='image-processing'>Image processing:</a>

#### [[⬆]](#toc) <a name='cryptography'>Cryptography:</a>
* [*Public-key cryptography*](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [*Public key certificate*](https://en.wikipedia.org/wiki/Public_key_certificate)
* [*Blockchain*](https://en.wikipedia.org/wiki/Blockchain)
* *RSA*
```
select 2 primes: p,q
n = p*q
phi(n) = (p-1)*(q-1)
select 1<e<phi(n), gcd(e,phi(n))=1
d=e^-1 mod phi(n)
(e,n) - public key
(d,n) - private key
c = m^e mod n
m = c^d mod n = m^(e*d) mod n = m^(e*d mod phi(n)) mod n = m
```

#### [[⬆]](#toc) <a name='security'>Security:</a>
* What is *OpenID and OAuth2.0 and OpenID Connect*?
* What is *access_token, SAML token, JWT token*?
* *Sticky session vs Session Replication*.
* What is *Federated Authentication* ?
* What is *CSP* and *SRI hash* ?
* What is *Clickjacking* and *Cursorjacking* ? How to prevent it ?

#### [[⬆]](#toc) <a name='android'>Android:</a>

#### [[⬆]](#toc) <a name='books'>Books:</a>
* [The C++ Programming Language, 4th Edition](https://www.amazon.com/C-Programming-Language-4th/dp/0321563840)
* [The Art of Multiprocessor Programming](https://www.amazon.com/Art-Multiprocessor-Programming-Revised-Reprint/dp/0123973376)
* [Effective Java (3rd Edition)](https://www.amazon.com/Effective-Java-3rd-Joshua-Bloch/dp/0134685997)
* [Java Concurrency in Practice](https://www.amazon.com/Java-Concurrency-Practice-Brian-Goetz/dp/0321349601)
* [Reactive Programming with RxJava](https://www.amazon.com/Reactive-Programming-RxJava-Asynchronous-Applications/dp/1491931655)
* [Introduction to Algorithms, 3rd Edition](https://www.amazon.com/Introduction-Algorithms-3rd-MIT-Press/dp/0262033844)
* [The Art of Computer Programming](https://www.amazon.co.uk/Art-Computer-Programming-Volumes-1-4a/dp/0321751043)
* [Network Flows: Theory, Algorithms, and Applications](https://www.amazon.com/Network-Flows-Theory-Algorithms-Applications/dp/013617549X)
* [Computational Geometry: Algorithms and Applications](https://www.amazon.com/Computational-Geometry-Applications-Mark-Berg/dp/3540779736)
* [Compilers: Principles, Techniques, and Tools](https://www.amazon.com/Compilers-Principles-Techniques-Tools-2nd/dp/0321486811)
* [Design Patterns: Elements of Reusable Object-Oriented Software](https://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
* [Big Data: Principles and best practices of scalable realtime data systems](https://www.amazon.com/Big-Data-Principles-practices-scalable/dp/1617290343)
* [Designing Data-Intensive Applications](https://www.amazon.com/Designing-Data-Intensive-Applications-Reliable-Maintainable/dp/1449373321)
* [Kafka: The Definitive Guide](https://www.amazon.com/Kafka-Definitive-Real-Time-Stream-Processing/dp/1491936169)
* [Cassandra: The Definitive Guide](https://www.amazon.com/Cassandra-Definitive-Guide-Distributed-Scale/dp/1491933666)
* [Hibernate in Action](https://www.amazon.com/Hibernate-Action-Christian-Bauer/dp/193239415X)
* [The Garbage Collection Handbook](https://www.amazon.com/Garbage-Collection-Handbook-Management-Algorithms/dp/1420082795)
* [Pro Git](https://git-scm.com/book/en/v2)
* [Learning JavaScript](https://www.amazon.com/Learning-JavaScript-Essentials-Application-Development/dp/1491914912)
* [The Busy Coder's Guide to Android Development](https://commonsware.com/Android/)
* [Clean Code: A Handbook of Agile Software Craftsmanship](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)
