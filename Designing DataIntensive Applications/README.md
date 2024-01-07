<center><h1>Designing Data-Intensive Application </h1></center>

A Data-intensive application is typically built from standard building blocks that provide commonly needed functionality.

    1. Store data so that they or another application can find it again later --> Database
    2. Remember the result of an expensive operation, to speed up reads --> Caches 
    3. Allow users to search data by keyword or filter it in various ways --> Search Indexes
    4. Send a message to another process, to be handled asynchronously --> Stream Processing
    5. Periodically crunch a large amount of accumulated data --> Batch Processing



3 Concerns that are important in software systems

    1. Reliability: 
            The System should continue to work correctly (performing the correct function at the desired level of performance) 
            even in the face of adversity ( Hardware or software faults and even human errors)


    2. Scalability:
            As the System grows (in data volume, traffic volume, or complexity) there should be a reasonable way of dealing with growth.

    3. Maintainability:
            Over time many different people will work on the system, and they should all work on it productively



<h2> Reliability </h2>

For software, typical expectations include:

    1. The application performs the function that the user expected
    2. It can tolerate the user making mistakes or using the software in unexpected ways
    3. Its performance is good enough for the required use case, under the expected load and data volume.
    4. The prevents any unauthorized access and abuse.

If all those things mean "working correctly", we can understand reliability as "Continuing to work 
correctly, even when things go wrong." 

The things that go wrong are called <b><i>Faults</i></b>

Systems that anticipate <b><i>Faults</i></b> and can cope with them are called <b><i>Fault-Tolerant</i></b> or <b><i>Resilient</i></b>

Note that a Fault is different from a Failure

Fault is usually defined as one component of a system deviating from Spec, whereas failure is when the system as a whole stops providing the required service to the user.

<h2> Scalability </h2>

If a system is working reliably today, that doesn't mean it will necessarily work reliably in the future. One common reason for degradation is increased load: perhaps an increase in user load or volume of data processing than it did before.

Scalability: Systems ability to cope with increased load.

Scalability means considering questions like 
    1. If the system grows in a particular way what are our options for coping with the growth?
    2. How can we add computing resources to handle the additional load?

Describe Load:

First, we need to describe the current load on the system only then we can discuss growth questions. Load can be described with a few numbers which we call Load Parameters.

Describe Performance:

Once you have described the load on your system, you can investigate what happens when the load increases. You can look at it in 2 ways

    1. When you increase a load parameter and keep the system resources(CPU, memory, network bandwidth, etc) unchanged, how is the performance of your system affected?
    2. When you increase a load parameter, how much do you need to increase the resources if you want to keep performance unchanged?

Approach for coping with Load:

Scale up or Vertical Scaling: Upgrading the hardware like RAM / Memory to cope with the increased load.

Scale out or Horizontal Scaling: Adding a new server to handle the increased load.


<h2> Maintainability:</h2>

The majority of the cost of software is not in its initial development but in its ongoing maintenance -- fixing bugs, keeping its systems operational, investigating failures, adapting it to new platforms, modifying it for new use cases, repaying technical debt, and adding new features.

We should design software in such a way that it hopefully minimizes pain during maintenance and thus avoids creating legacy software ourselves. We will pay particular attention to three design principles for software systems

    1. Operability: Make it easy for operations teams to keep the system running smoothly.
    2. Simplicity: Make it easy for new engineers to understand the system, by removing as much complexity as possible from the system.
    3. Evolvability: Make it easy for engineers to make changes to the system in the future, adapting it for unanticipated use cases as requirements change. Also known as Extensibility, Modifibility or Plasticity


<h4>Operability:</h4>

Operations teams are vital to keeping a software system running smoothly. A good operations team typically is responsible for the following

    1. Monitoring the health of the system and quickly restoring service if it goes into a bad state
    2. Tracking down the cause of problems, such as system failure or delegated performance
    3. keeping software and platform up to date 
    4. Keeping tabs on how different systems affect each other so that a problematic change can be avoided before it causes damage
    5. Anticipating future problems and solving them before they occur(eg; Capacity planning)
    6. Establishing good practices and tools for deployment, configuration management, and more 
    7. Performing complex maintenance tasks such as moving applications from one platform to another
    8. Maintaining the security of the system as configuration changes are made
    9. Define processes that make operations predictable and help keep the production environment stable
    10. Preserving the organization's knowledge about the system, even individual people come and go

Good operability means making routine tasks easy, allowing the operations team to focus their efforts on high-value activities. Data systems can do various things to make routine tasks easy, including:

    1. Providing visibility into the runtime behavior and internals of the system, with good monitoring
    2. Providing good support for automation and integration with standard tools
    3. Avoiding dependency on individual machines(allowing machines to be taken down for maintenance while the system as a whole continues running uninterrupted)
    4. Providing good documentation and an easy-to-understand operational model
    5. Providing good default behavior, but also giving the administrator the freedom to override defaults when required
    6. Self-healing where appropriate but also giving administrators manual control over the system when needed
    7. Exhibiting predictable behavior, minimizing surprises


<h4> Simplicity:</h4>
Small software projects can have delightfully simple and expressive code, but as projects get larger, they often become very complex and difficult to understand. This complexity slows down everyone who is working on the system, further increasing the cost of maintenance. 

One of the best tools for removing complexity is abstraction, A good abstraction can hide a great deal of implementation detail behind a clean simple-to-understand facade.



<h4> Evolvability:</h4>

In terms of organizational processes, Agile working patterns provide a framework for adapting to changes. Most discussions of these Agile techniques focus on fairly small and local scales.


<center><h1>Data Models and Query Launguages</h1></center>

1. Relation Database
2. NoSql Database










    




