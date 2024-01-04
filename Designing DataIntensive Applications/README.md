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




    




