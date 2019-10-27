1. What is Brog?
Brog is a cluster manager for large-scale resource management.
2. What are the problems the paper wants to solve?
This paper explains the system which admits, schedules, starts, restarts, and monitors the full range of applications that Google runs.
3. What are the key benefits of Brog?
First, hide the details from users.
Second, high availability.
Third, run tasks effectively.
4. How about the tasks running on Brog?
The first kind of task is long-running (which calls for high availability), such as the back end service for Google search.
The second kind of task is batch jobs (which call for high performance in a short time), such as analysis on large amounts of data.
What's worse, every job has specific needs. For example, one batch job may complete in two days, but another batch job may only take two seconds. The workload also varies over time.
5. What is the structure of Borg?
The Borg has a hierarchical structure in which one median cell has ten thousand machines. However, the master of the layer manages all the resources of the machine and isolate all the actual detail of these machines from the users.
6. How to run a bunch of tasks together?
Borg created a term called "Allocs", which is a reserved set of resources. To meet the needs of one allow, the Borg can relocate Alloc to another machine.
7. Are all tasks created equal?
Not exactly. Every task in Brog has a different priority. A low-priority job might be kicked out by a high-priority job if the resource is not sufficient for all of them.
Every task can specify its needs in "Quota", such as CPU, GPU, etc
8. How does Borg get data about the running tasks?
Just like today's microservice framework, Brog has a naming service which records the task's hostname, port and put it into high-available consistent storage.
When it comes to the running task, it has to provide HTTP based metrics and user-interface about the state of the task. What's more, this kind of pre-task information is also used to make future decisions and analysis of Borg.
9. What is the controller of a cell?
The controller of a cell has five replicas and a scheduler. In this way, the controller is highly-available.
What's more, the controller also stores the data on separate storage so that each controller can recover from that, and it is also used for debugging.
10. How does Brog schedule the tasks?
There is no denying that assigning a score to each candidate is the most common way to schedule the task, but how to give a score to a certain task is quite obscure. It is worth noticing that having the packages which 
are going to be used is an important factor because installing packages took a long time. Apart from that, spreading the small tasks or put them together is a trade-off, the former one provides better high-availability, but the latter one is good for large tasks.
11. How to scale up the scheduler?
The paper gives out three approaches to do this: cache the score until the condition changes put candidates into classes and randomly pick candidates.
12. How to make the tasks highly-available?
From the task's perspective, setting multiple replications, storing state and taking additional checkpoints are helpful.
From the Borg's perspective, rescheduling automatically, spreading tasks on different machines, limiting the times of retrying are helpful.
13. How to improve the performance of Borg?
First, the paper pointed out that run prod and non-prod jobs together can use fewer machines to run the same workload.
Second, the paper pointed out that using dedicated cells rather than shared cells can have better performance. However, it turns out that the benefit of using fewer machines with shared cells outweighs the benefit of dedicated cell
Third, the paper says that from the perspective of large tasks, large cells will reduce fragmentation, which means consuming fewer resources.
14. What about oversubscription in Brog?
Brog estimates a task's resource usage once every few seconds, and use other resources to run a batch job, this can greatly increase efficiency.
15. How does Brog isolate resources between different tasks?
Running different tasks on one machine can improve utilization. Brog ensures that the long-running, latency-senstive tasks are running and kills tasks that consume more resources than they should.