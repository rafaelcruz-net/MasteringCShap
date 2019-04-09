#EXERCISE MODULE 4

#### 1 - Remove an item from the list. Above the sample code.   

```csharp
using System;
using System.Collections.Generic;

public class Program
{
    public static void Main()
    {
        List<string> characters = new List<string>()
        {
            "Luke Skywalker",
            "Han Solo",
            "Chewbacca"
        };
        
        // Your code goes here.
    }
}
```

#### 2 - Adding a item to a list except if the name is 'Explorer.exe'. Above the sample code

```csharp
public static List<string> ProcessToKill(List<string> process)
{
    // Create list of string with initial size to 3.
    List<string> processToKill = new List<string>(3);

    // Show capacity ; here : 3.
    Console.WriteLine(string.Format("Capacity {0}", processToKill.Capacity));

    // Show number of items ; here : 0.
    Console.WriteLine(string.Format("Count {0}", processToKill.Count));

    /// TODO: 
    /// Add items from process to processToKill list 
    /// Process equals "Explorer.exe" don't be added, ignore it


    foreach (var p in processToKill)
    {
        Console.WriteLine(p);
    }           

    return processToKill;
}
```

#### 3 - Which of the following types is a reference type?
(   )Option 1: Boolean
(   )Option 2: Byte
(   )Option 3: Decimal
(   )Option 4: Int32
(   )Option 5: Object

#### 4 - Which of the following types of member CANNOT be included in an interface?
(   )Option 1: Events
(   )Option 2: Fields
(   )Option 3: Indexers
(   )Option 4: Methods
(   )Option 5: Properties


#### 5 - You want to create a custom generic class. The class will consist of a linear collection of values, and will enable developers to queue items from either end of the collection. Which of the following should your class declaration resemble?
(   )Option 1: public class DoubleEndedQueue<T> : IEnumerable<T>
(   )Option 2: public class DoubleEndedQueue<T> : ICollection<T>
(   )Option 3: public class DoubleEndedQueue<T> : IList<T>
(   )Option 4: public class DoubleEndedQueue<T> : IList<T>, IEnumerable<T>
(   )Option 5: public class DoubleEndedQueue<T> : IDictionary<TKey,TValue>

#### 6 - Which of the following types of method must you implement in derived classes?
(   )Option 1: Abstract methods.
(   )Option 2: Protected methods.
(   )Option 3: Public methods.
(   )Option 4: Static methods.
(   )Option 5: Virtual methods.

#### 7 - You want to create an extension method for the String class. You create a static method within a static class. How do you indicate that your method extends the String type?
(   )Option 1: The return type of the method must be a String.
(   )Option 2: The first parameter of the method must be a String.
(   )Option 3: The class must inherit from the String class.
(   )Option 4: The method declaration must include String as a type argument.
(   )Option 5: The method declaration must be preceded by String.



