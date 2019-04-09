# ANSWERS MODULE 2

#### EXERCISE 1

```csharp
using System;
class funcexer
{
    public static int Fibo(int nno)
    {
        int num1 = 0;
        int num2 = 1;
        
        for (int i = 0; i < nno; i++)
        {
            int temp = num1;
            num1 = num2;
            num2 = temp + num2;
        }
            return num1;
    }

    public static void Main()
    {
        Console.Write("\n\nFunction : To display the n number Fibonacci series :\n");
        Console.Write("------------------------------------------------------------\n");
        Console.Write("Input number of Fibonacci Series : ");
        int n= Convert.ToInt32(Console.ReadLine());
        
        Console.WriteLine("The Fibonacci series of "+n+" numbers is :");	  
        for (int i = 0; i < n; i++)
        {
            Console.Write(Fibo(i)+"  ");
        }
        
        Console.WriteLine();
    }

}

#### EXERCISE 2

```csharp
using System;
public class TrySqrt
{
    public static void Main()
    {
        float result;
        float num;
 
        Console.Write("Enter Number ");
        try
        {
            num = Convert.ToSingle(Console.ReadLine());
 
            result = (float)Math.Sqrt(num);
            Console.WriteLine("The result is: {0}", result);
        }
        catch (Exception)
        {
            Console.WriteLine("Error, I cannot calculate the Square Root");
        }
    }
}
```

### EXERCISE 3

**(X) FALSE**

> A finally block will run code irrespective of whether an exception occurs. A catch block enables you to run code if an error occurs.

### EXERCISE 4

**(X) TRUE**

> Trace statements are active in both Debug and Release mode builds.
However, Debug statements are only active if you build your solution in Debug mode.

### EXERCISE 5

**(X) OPTION 3**

> You must assign a value to an output parameter before the method returns, otherwise your code will not compile.




