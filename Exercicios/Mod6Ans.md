# EXERCISES  MODULE 6

#### EXERCISE 2
```csharp
using System;
using System.Linq;
using System.Collections.Generic;
 
class LinqExercise
{
 static void Main(string[] args)
    {
    // code from DevCurry.com
    var arr1 = new[] { 3, 9, 2, 8, 6, 5 };

            Console.Write("\nLINQ : Find the number and its square of an array which is more than 20 : "); 
            Console.Write("\n------------------------------------------------------------------------\n");	
	
    var sqNo = from int Number in arr1
                    let SqrNo = Number * Number
                    where SqrNo > 20
                    select new { Number, SqrNo };

    foreach (var a in sqNo)
        Console.WriteLine(a);

    Console.ReadLine();
    }
}
```


#### EXERCISE 3 
```csharp
using System;
using System.Linq;
using System.Collections.Generic;
 
class LinqExercise
{
    static void Main(string[] args)
    {
         int[] arr1 = new int[] { 5, 9, 1, 2, 3, 7, 5, 6, 7, 3, 7, 6, 8, 5, 4, 9, 6, 2 };  
         Console.Write("\nLINQ : Display the number and frequency of number from given array : \n"); 
         Console.Write("---------------------------------------------------------------------\n");
         Console.Write("The numbers in the array  are : \n");
         Console.Write(" 5, 9, 1, 2, 3, 7, 5, 6, 7, 3, 7, 6, 8, 5, 4, 9, 6, 2\n");
			
		var n = from x in arr1  
				group x by x into y  
				select y;  
		
        Console.WriteLine("\nThe number and the Frequency are : \n"); 
		
        foreach (var arrNo in n)  
		{  
			Console.WriteLine("Number "+arrNo.Key + " appears " + arrNo.Count()+" times");  
		} 
        Console.WriteLine("\n");				
    }
}

```

#### EXERCISE 4

**LINQ provides compile-time syntax-checking and type-checking and IntelliSense support in Visual Studio.**
