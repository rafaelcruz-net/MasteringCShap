# ANWSERS MODULE 1

### EXERCISE 1

```csharp
using System;  
public class Exercise 
{  
   public static void Main() 
   {
        int num1,num2,opt;

        Console.Write("\n\n");
        Console.Write("A menu driven program for a simple calculator:\n");
        Console.Write("------------------------------------------------");
        Console.Write("\n\n");


        Console.Write("Enter the first Integer :");
        num1 = Convert.ToInt32(Console.ReadLine());
        Console.Write("Enter the second Integer :");
        num2 = Convert.ToInt32(Console.ReadLine());

  
        Console.Write("\nHere are the options :\n");
        Console.Write("1-Addition.\n2-Substraction.\n3-Multiplication.\n4-Division.\n5-Exit.\n");
        Console.Write("\nInput your choice :");
        opt = Convert.ToInt32(Console.ReadLine());

        switch(opt) 
        {
            case 1:
                Console.Write("The Addition of  {0} and {1} is: {2}\n",num1,num2,num1+num2);
                break;
                
            case 2:
                Console.Write("The Substraction of {0}  and {1} is: {2}\n",num1,num2,num1-num2);
                break;
                
            case 3:
                Console.Write("The Multiplication of {0}  and {1} is: {2}\n",num1,num2,num1*num2);
                break;  
            
            case 4:
                if(num2==0) {
                Console.Write("The second integer is zero. Devide by zero.\n");
                } else {
                Console.Write("The Division of {0}  and {1} is : {2}\n",num1,num2,num1/num2);
                }  
                break;
                
            case 5: 
                break; 
                
            default:
                Console.Write("Input correct option\n");
            break; 
        }
    }
}
```


### EXERCISE 2:

```csharp
using System;
public class Exercise
{
  public static void Main()
  {
   Console.Write("Input a number: ");
   int num = Convert.ToInt32( Console.ReadLine() );
 
   Console.Write("Input the desired width: ");
   int width = Convert.ToInt32( Console.ReadLine() );
 
   int height = width;   
   for (int row=0; row < height; row++)
   {
    for (int column=0; column < width; column++)
   {
   Console.Write( num );
  }
 
   Console.WriteLine();
   width--;
  }
 }
} 
```


### EXERCISE 3

```csharp
using System;  
public class Exercise
{  
    public static void Main() 
    {             
        int i,n,sum=0;
        double avg;
        
        Console.Write("\n\n");
        Console.Write("Read 10 numbers and calculate sum and average:\n");
        Console.Write("----------------------------------------------");
        Console.Write("\n\n");
        
        Console.Write("Input the 10 numbers : \n");
        for (i=1;i<=10;i++)
        {
                    Console.Write("Number-{0} :",i);

            n= Convert.ToInt32(Console.ReadLine());		
            sum +=n;
        }
        avg=sum/10.0;
        Console.Write("The sum of 10 no is : {0}\nThe Average is : {1}\n",sum,avg);
   }
}
```