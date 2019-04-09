# EXERCISE MODULE 3

#### 1 - Write a program in C# Sharp to declares a struct with a property, a method, and a private field.

#### 2 - Write a program in C# Sharp to insert the information of two books.

>Insert the information of two books :                    
>-----------------------------------------                
>Information of book 1 :                                  
>Input name of the book : BASIC                           
>Input the author : S.TROELSTRA                           
>                                                         
>Information of book 2 :                                  
>Input name of the book : C+                              
>Input the author : G.RTRTG 
>                              
>Expected Output:
>1: Title = BASIC,  Author = S.TROELSTRA                  
>2: Title = C+,  Author = G.RTRTG 

#### 3 - You want to create a string property named CountryOfOrigin. You want to be able to read the property value from any code, but you should only be able to write to the property from within the containing struct. How should you declare the property? 
(   )Option 1: public string CountryOfOrigin { get; set; }
(   )Option 2: public string CountryOfOrigin { get; }
(   )Option 3: public string CountryOfOrigin { set; }
(   )Option 4: public string CountryOfOrigin { get; private set; }


#### 4 - You want to create a collection to store coffee recipes. You must be able to retrieve each coffee recipe by providing the name of the coffee. Both the name of the coffee and the coffee recipe will be stored as strings. You also need to be able to retrieve coffee recipes by providing an integer index. Which collection class should you use?
(   )Option 1: ArrayList
(   )Option 2: Hashtable
(   )Option 3: SortedList
(   )Option 4: NameValueCollection
(   )Option 5: StringDictionary


#### 5 - You are creating a method to handle an event named OutOfBeans. The delegate for the event is as follows:
```csharp
public delegate void OutOfBeansHandler(Coffee coffee, EventArgs args);
```
Which of the following methods should you use to subscribe to the event?
(   )Option 1: public void HandleOutOfBeans(delegate OutOfBeansHandler)
(   )Option 2: public void HandleOutOfBeans(Coffee c, EventArgs e)
(   )Option 3: public Coffee HandleOutOfBeans(EventArgs e)
(   )Option 4: public Coffee HandleOutOfBeans(Coffee coffee, EventArgs args)
(   )Option 5: public void HandleOutOfBeans(Coffee coffee)
