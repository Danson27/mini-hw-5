link to repo https://github.com/Danson27/mini-hw-5/edit/main/README.md Explanations: Task 3: expected 20,000 Actual result: non-deterministic output, 16536 This is a product of Race Condition. bar++ is three steps, and since it is not atomic, we can have collisions. Thread 1 can be paused by the OS mid run

Tasl 4: expected and actual result: 20,000 here, we locked it using the the built in lock using synchronized. any thread using the method must acquire Foo's lock. Once thread 1 is inside baz, thread 2 is locked out. Furthermore, because getBar() is also synchronized, a thread cannot even read the variable while another thread is mutating it, preventing dirty reads and guaranteeing perfect data integrity.

Task 5: expected and actual result: 20,000 Here, we introduced the concept Lock Granularity.

Task 6:
Output: 33052080 80 this code will run very fast because we have 10 threads that run concurrently across many CPU cores with no stop and waits. But since the memory is unprotected, the data suffers from race conditions, losing nearly 70 million updates to thread collisions.

Task 7: output: 100000000 12464

we hit 100000000 showing that the lock works. but we went from 80 milliseconds to 12 seconds. locks are very time expensive.