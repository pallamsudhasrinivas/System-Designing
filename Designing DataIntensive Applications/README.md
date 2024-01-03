<center><h1>Designing Data-Intensive Application </h1></center>

A Data intensive application is typically build from standard building blocks that provide commonly needed functionality.

    1. Store data so that they or another application can find it again later --> Database
    2. Remember the result of an expensive operation, to speed up reads --> Caches 
    3. Allow users to search data by keyword or filter it in various ways --> Search Indexes
    4. Send a message to another process, to be handeled asynchronously --> Stream Processing
    5. Periodically crunch a large amount of accumulated data --> Batch Processing



3 Concerns that are important in software systems

    1. Reliability: 
            The System should continue to work correctly (performing the correct function at the desired level of performance) 
            even in the face of adversity ( Hardware or software faults and even human erros)


    2. Scalability:
            As the System grows (in data volume, traffic volume or complexity) there should be resonable way of dealing eith growth.

    3. Maintainability:
            Over time many different people will work on the system, and they should all work on it productively



<h2> Reliability </h2>

For software, typical expectations include:

    1. The application performs the function that the user expected
    2. It can tolerate the user making mistakes or using the software in unexpected ways
    3. Its performance is good enough for the required use case, under the expected load and data volume.
    4. The prevents any unauthorized access and abuse.

If all those things means "working correctly", we can understand reliability as "Continuing to work 
correctly, even when things go wrong." 

The things that go wrong are called <b><i>Faults</i></b>

Systems that anticipate <b><i>Faults</i></b> and can cope with them are called <b><i>Fault-Tolerant</i></b> or <b><i>Resilient</i></b>

Note that a Fault is different from Failure

Fault is usually define as one component of a system deviating from Spec, where as failure is when the system as a whole stops providing the required service to the user.

