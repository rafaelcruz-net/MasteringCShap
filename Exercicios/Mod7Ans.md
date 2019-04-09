# ANSWER MODULE 7

#### EXERCISE 1

```csharp
 static void Main(string[] args)
{
    CancellationTokenSource cancellationTokenSource = new CancellationTokenSource();
    CancellationToken cancellationToken = cancellationTokenSource.Token;

    Task taskOne = Task.Factory.StartNew(() =>
    {
        for (int i = 0; i < 10; i++)
        {
            cancellationToken.ThrowIfCancellationRequested();
            Console.WriteLine(i);
            cancellationToken.WaitHandle.WaitOne(1000);
        }
        Console.WriteLine("Task 1 complete");
    }, cancellationToken);

    Task taskTwo = Task.Factory.StartNew(() =>
    {
        for (int i = 0; i < 5; i++)
        {
            cancellationToken.ThrowIfCancellationRequested();
            Console.WriteLine(i);
            cancellationToken.WaitHandle.WaitOne(500);
        }
        Console.WriteLine("Task 2 complete");
    }, cancellationToken);

    Task.WaitAll(taskOne, taskTwo);

    Console.Read();

}

```

#### EXERCISE 2

```csharp
static void Main(string[] args)
{
    Task firstTask = Task.Factory.StartNew(() =>
    {
        ArgumentNullException exception = new ArgumentNullException();
        exception.Source = "First task";
        throw exception;
    });
    Task secondTask = Task.Factory.StartNew(() =>
    {
        throw new ArgumentException();
    });
    Task thirdTask = Task.Factory.StartNew(() =>
    {
        Console.WriteLine("Hello from the third task.");
    });

    try
    {
        Task.WaitAll(firstTask, secondTask, thirdTask);
    }
    catch (AggregateException ex)
    {
        foreach (Exception inner in ex.InnerExceptions)
        {
            Console.WriteLine("Exception type {0} from {1}",
                inner.GetType(), inner.Source);
        }
    }

    Console.Read();
}

```

#### EXERCISE 3

```csharp
 class Program
{
    static void Main(string[] args)
    {
        BankAccount account = new BankAccount();
        List<Task> tasks = new List<Task>();
        object lockObject = new object();

        for (int i = 0; i < 5; i++)
        {
            tasks.Add(Task.Factory.StartNew(() =>
            {
                for (int j = 0; j < 1000; j++)
                {
                    lock (lockObject)
                    {
                        account.Balance = account.Balance + 1;
                    }
                }
            }));
        }
        Task.WaitAll(tasks.ToArray());
        Console.WriteLine(string.Concat("Expected value 5000", ", actual value ", account.Balance));

    }
}

class BankAccount
{
    public int Balance { get; set; }
}


```


#### EXERCISE 4

**(X) Option 2: Task.WaitAll(task1, task2, task3);**

>If you need to wait for multiple tasks to complete before you continue, you should use the static Task.WaitAll method.


#### EXERCISE 5

**(X) Option 3: public async Task\<IEnumerable\<string>> GetCoffees(string country, int strength)**

>If a synchronous method has a return type of T, the asynchronous equivalent should have a return type of Task<T>. In this case, the return type becomes Task\<IEnumerable\<string>>.

#### EXERCISE 6

**(X) Option 2: The SemaphoreSlim class.**

>The SemaphoreSlim class enables you to specify an integer value that represents the number of threads that can access a resource. When a thread accesses the resource, the counter is decremented. When the thread is finished with the resource, the counter is incremented. If the counter reaches zero, a thread must wait until the counter returns to a non-zero value before it can access the resource.