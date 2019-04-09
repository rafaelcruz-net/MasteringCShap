# ANSWER MODULE 3


#### EXERCISE 1

```csharp
using System;
struct newStruct
{
    private int num;

    public int n
    {
        get 
        {
            return num;
        }
        set 
        {
            num = value;
        }
    }
    public void Print()
    {
        Console.WriteLine("\nThe stored value is: {0}\n", num);
    }
}

class Exercise
{
    public static void Main()
    {
		Console.Write("\n\nDeclares a struct with a property, a method, and a private field :\n");
		Console.Write("----------------------------------------------------------------------\n");	
        newStruct myInstance = new newStruct();
        myInstance.n = 15;
        myInstance.Print();
    }
}

```

#### EXERCISE 2

```csharp
using System;

struct book 
{
	public string title;
	public string author;
}
public class strucExer9
{
    public static void Main ()  
	{
        int nobook = 2;  
        book[] books =new book [nobook];   
        
        Console.Write("\n\nInsert the information of two books :\n");
        Console.Write("-----------------------------------------\n");    
        
        for(var i=0; i<nobook;i++)
        {
            Console.WriteLine("Information of book {0} :",i+1);

            Console.Write("Input name of the book : ");
            books[i].title= Console.ReadLine();

            Console.Write("Input the author : ");
            books[i].author= Console.ReadLine();
           
            Console.WriteLine();
        }

        for(var i=0;i<=nobook;i++)
        {
            Console.WriteLine("{0}: Title = {1},  Author = {2}", i+1, books[i].title, books[i].author);
            Console.WriteLine();
        }
	}
}

```

#### EXERCISE 3

**(X) Option 4: public string CountryOfOrigin { get; private set; }**

>You can use access modifiers on property accessors to provide more granular control over where your property is accessed from. If you mark the set accessor as private, you will only be able to set the value of the property from within the containing struct or class.

#### EXERCISE 4

**(X) Option 4: NameValueCollection**

>In this scenario you are storing key/value pairs—the name of the coffee is the key, and the recipe is the value—so you must use a dictionary collection. The ArrayList is a list collection, so it is unsuitable. Because both your key and your value will always be strings, you should use a strongly typed string dictionary. NameValueCollection and StringDictionary are both strongly typed string dictionary classes. However, the StringDictionary class does not allow you to retrieve items by index, so the correct answer is NameValueCollection.

#### EXERCISE 5

**(X) Option 2: public void HandleOutOfBeans(Coffee c, EventArgs e)**

> To subscribe to an event, the event handler method must match the signature of the event delegate. This means that the method must have the same return type and the same parameters as the delegate. The name of the method does not need to match the name of the delegate, and the names of the method parameters do not need to match the names of the delegate parameters.



