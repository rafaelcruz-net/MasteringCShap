# EXERCISE MODULE 7

#### 1 - Create a program that waits a group of task. All task is just a simple loop and prints de indexes number on console. All tasks must receive a cancellation token.


#### 2 - Create a program that create a group of task and one of this task send a exception. Wrap all exceptions gracefull.


#### 3 - Create a program thats calculate the balance of an account. Use multitask programming to calculate the balance. Use lock statement to prevent concurrence

#### 4 - You create and start three tasks named task1, task2, and task3. You want to block the joining thread until all of these tasks are complete. Which code example should you use to accomplish this?
(   )Option 1: task1.Wait(); task2.Wait(); task3.Wait();
(   )Option 2: Task.WaitAll(task1, task2, task3);
(   )Option 3: Task.WaitAny(task1, task2, task3);
(   )Option 4: Task.WhenAll(task1, task2, task3);
(   )Option 5: Task.WhenAny(task1, task2, task3);

#### 5 - You have a synchronous method with the following signature: You have a synchronous method with the following signature: public IEnumerable\<string> GetCoffees(string country, int strength). You want to convert this method to an asynchronous method. What should the signature of the asynchronous method be?

(   )Option 1: public async IEnumerable\<string> GetCoffees(string country, int strength)
(   )Option 2: public async Task\<string> GetCoffees(string country, int strength)
(   )Option 3: public async Task\<IEnumerable\<string>> GetCoffees(string country, int strength)
(   )Option 4: public async Task GetCoffees(string country, int strength, out string result)
(   )Option 5: public async Task GetCoffees(string country, int strength, out IEnumerable\<string> result)

#### 6 - You want to ensure that no more than five threads can access a resource at any one time. Which synchronization primitive should you use?

(   )Option 1: The ManualResetEventSlim class.
(   )Option 2: The SemaphoreSlim class.
(   )Option 3: The CountdownEvent class.
(   )Option 4: The ReaderWriterLockSlim class.
(   )Option 5: The Barrier class.
