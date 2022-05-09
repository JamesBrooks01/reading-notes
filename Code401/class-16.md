# Reading Assignment 16

## Serverless Functions

---

### What is Serverless Computing?

---

- Serverless is a cloud execution model that allows a simpler, more cost-effective way to build and operate cloud-native applications.
- The Serverless Model;
  - Perfomrs the automatic provisioning of computing resources that are required to run the application code.
  - Scales the resourses up or down to meet demand.
  - Scales to 0 when the application stops running.
- It offloads all the management to the cloud provider allowing developers more time to develop and optimize the front-end.
- Serverless and FaaS are often conflated but FaaS is actually a subset of Serverless that is the computational paradigm that is central to the Serverless process that has the code or containers only run in response of an event or request.
- There are of course Pros and Cons to Serverless;
  - Pros
    - Allows dev teams to focus on writing code rather than managing infrastructure.
    - Customers only pay for execution, the "meter" starts when the request starts and ends when the execution finishes.
    - A polygot enviroment allowing developers to code in whatever language or framework they are most comfortable with.
    - Simplifies development because developers don't have to descibe infrastucte for integrating, testing, delivering, and deploying code builds into production.
    - For certain workloads, Serverless can be faster and more cost-effective
    - Allow near-total visibility for system and user times and can aggregate the information systematically
  - Cons
    - Because of the scaling nature of Serverless, it offers significant cost savings for spiky workloads, but is not as cost-effective when working with a predictable, steady or long-running process where a traditional server enviroment is often simpler and more cost effective.
    - Because Serverless forgos long-running procceses in favor of scaling up and sown, they sometimes need to start up from zero to process a request, for some applications this delay isn't noticable or detrimental, but for some, like Financial Trading, this delay is unacceptable.
    - Standard servers are already difficult to monitor and debug, but the nature of Serverless Arcitecture only makes this task more difficult as it is difficult to use existing tools and processes for the task.
    - Serverless architecture is designed to take advantage of an ecosystem of cloud services and works hard to decouple a workload. For some companies this decoupling is where much of the value for the cloud is, but for others is a material lock-in that needs to be mitigated.

---

### What is Serverless?

---

- Serverless doesn't actually mean no servers, it just means that the customer is not responsible for managing and provisioning the servers.
- Part of Serverless is Function As A Service(FaaS). FaaS works off the system of "events" to run the processes. An event can be anything. It is something that happens which then calls a function that runs the code.
- Serverless apps are Highly Available
  - Cloud Providers take care of the Fault Tolerance and MZRs(Multi-Zone Regions) that are built to ensure the app is always up and running.
