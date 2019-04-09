# ANSWERS MODULE 4

#### EXERCISE 1

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
        
        characters.Remove("Luke Skywalker");
    }
}
```

#### EXERCISE 2

```csharp
public static List<string> ProcessToKill(List<string> process)
{
    // Create list of string with initial size to 3.
    List<string> processToKill = new List<string>(3);

    // Show capacity ; here : 3.
    Console.WriteLine(string.Format("Capacity {0}", processToKill.Capacity));

    // Show number of items ; here : 0.
    Console.WriteLine(string.Format("Count {0}", processToKill.Count));

    foreach (var p in process) 
    { 
        if (!p.Equals("Explorer.exe")) 
        { 
            processToKill.Add(p); 
            
        } 
    }

    foreach (var p in processToKill)
    {
        Console.WriteLine(p);
    }           

    return processToKill;
}
```

#### EXERCISE 3
**(X) Option 5: Object**

>All the built-in types except Object and String are value types. They are defined by structs rather than by classes

#### EXERCISE 4
**(X) Option 2: Fields**

>You cannot include fields when you define an interface. This is because fields are a detail of implementation, rather than a definition of externally available functionality.

#### EXERCISE 5
**(X) Option 3**

>The IEnumerable<T> interface has the least functionality, compared to the rest. Only exposing the ability to go over its items one by one. All the other interfaces will each add its own methods that will break the demands of only allowing the user to enqueue and dequeue from both ends. IList<T>, for example will add the Insert and RemoveAt methods that allows manipulating values at arbitrary indexes

#### EXERCISE 6

**(X) Option -1: Abstract methods.**

>An abstract method is like a method declaration in an interface—it does not include an implementation. When you inherit from an abstract class, you must provide implementations for any abstract members.

#### EXERCISE 7

**(X) Option - 2: The first parameter of the method must be a String.**

>To create an extension method for the String type, the first parameter must be a String. To indicate that your method extends the String type, the parameter must also be preceded by the this keyword.
