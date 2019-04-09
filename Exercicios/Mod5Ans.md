# ANSWER MODULE 5

### EXERCISE 1

```csharp
using System;
using System.IO;
using System.Text;

class filexercise
{
    public static void Main()
    {
        string fileName = @"mytest.txt";

        try
        {
            // Delete the file if it exists.
            if (File.Exists(fileName))
            {
                File.Delete(fileName);
            }
			Console.Write("\n\n Create a file with content in the disk :\n");
			Console.Write("---------------------------------------------\n");            
            // Create the file.
            using (StreamWriter fileStr = File.CreateText(fileName)) 
            {
                fileStr.WriteLine(" Hello and Welcome");
                fileStr.WriteLine(" It is the first content");
                fileStr.WriteLine(" of the text file mytest.txt");
				 Console.WriteLine(" A file created with content name mytest.txt\n\n");
            }	            			
        }
        catch (Exception MyExcep)
        {
            Console.WriteLine(MyExcep.ToString());
        }
    }
}

```
### EXERCISE 2
```csharp
using System;
using System.IO;
using System.Text;

class filexercise
{
    public static void Main()
    {
        string fileName = @"mytest.txt"; 

        try
        {
            // Delete the file if it exists.
            if (File.Exists(fileName))
            {
                File.Delete(fileName);
            }
			Console.Write("\n\n Create a file with text and read the file  :\n");
			Console.Write("-------------------------------------------------\n");            
            // Create the file.
            using (StreamWriter fileStr = File.CreateText(fileName)) 
            {
                fileStr.WriteLine(" Hello and Welcome");
                fileStr.WriteLine(" It is the first content");
                fileStr.WriteLine(" of the text file mytest.txt");
            }	            
            using (StreamReader sr = File.OpenText(fileName))
            {
                string s = "";
				Console.WriteLine(" Here is the content of the file mytest.txt : ");
                while ((s = sr.ReadLine()) != null)
                {
                    Console.WriteLine(s);
                }
                Console.WriteLine("");
            }
        }
        catch (Exception MyExcep)
        {
            Console.WriteLine(MyExcep.ToString());
        }
    }
}

```

#### EXERCISE 3

```csharp
using System;
using System.IO;
using System.Text;

class filexercise
{
    public static void Main()
    {
        string fileName = @"mytest.txt"; 
        try
        {
            // Delete the file if it exists.
            if (File.Exists(fileName))
            {
                File.Delete(fileName);
            }
			Console.Write("\n\n Append some text to an existing file  :\n");
			Console.Write("--------------------------------------------\n");            
            // Create the file.
            using (StreamWriter fileStr = File.CreateText(fileName)) 
            {
                fileStr.WriteLine(" Hello and Welcome");
                fileStr.WriteLine(" It is the first content");
                fileStr.WriteLine(" of the text file mytest.txt");
            }	            
            using (StreamReader sr = File.OpenText(fileName))
            {
                string s = "";
				Console.WriteLine(" Here is the content of the file mytest.txt : ");
                while ((s = sr.ReadLine()) != null)
                {
                    Console.WriteLine(s);
                }
                Console.WriteLine("");
            }
        using (System.IO.StreamWriter file = new System.IO.StreamWriter(@"mytest.txt", true))
        {
            file.WriteLine(" This is the line appended at last line.");
        }
              using (StreamReader sr = File.OpenText(fileName))
            {
                string s = "";
				Console.WriteLine(" Here is the content of the file after appending the text : ");
                while ((s = sr.ReadLine()) != null)
                {
                    Console.WriteLine(s);
                }
                Console.WriteLine("");
            }          
            
        }
        catch (Exception MyExcep)
        {
            Console.WriteLine(MyExcep.ToString());
        }
    }
}

```

#### EXERCISE 4

```csharp

namespace Serialize
{
    class Program
    {
        static void Main(string[] args)
        {
            var @class = new SerializeClass()
            {
                Address = "Street Tests",
                DateTime = DateTime.Now,
                Name = "Test Data"
            };

            var outputBin = @class.SearializeBinary();

            var outputXML = @class.SearializeXML();

            var outputJson = @class.SearializeJson();

            string result = String.Empty;

            foreach (var item in outputBin)
                result += $"{item.ToString("X2")}";

            Console.WriteLine(result);

            Console.WriteLine(outputXML);

            Console.WriteLine(outputJson);

            Console.ReadKey();

        }
    }


    [Serializable]
    public class SerializeClass
    {
        public string Name { get; set; }
        public DateTime DateTime { get; set; } 

        public string Address { get; set; }

        public byte[] SearializeBinary()
        {
            BinaryFormatter binaryFormatter = new BinaryFormatter();
            MemoryStream ms = new MemoryStream();
            binaryFormatter.Serialize(ms, this);

            return ms.ToArray();
            
        }

        public String SearializeXML()
        {
            XmlSerializer formatter = new XmlSerializer(typeof(SerializeClass));
            MemoryStream ms = new MemoryStream();
            formatter.Serialize(ms, this);
            return Encoding.Default.GetString(ms.ToArray());

        }

        public String SearializeJson()
        {
            DataContractJsonSerializer serializer = new DataContractJsonSerializer(typeof(SerializeClass));
            MemoryStream ms = new MemoryStream();
            serializer.WriteObject(ms, this);
            return Encoding.Default.GetString(ms.ToArray());

        }


    }
}

```

#### EXERCISE 5
**The JsonConvert class.** 
>Since the persisted data needs to be human readable, you should use the JsonConvert class.

#### EXERCISE 6

**(X) Option 2: The FileStream, BinaryReader and BinaryWriter classes.**

>You should use the FileStream class to access the file system, and then the BinaryReader and BinaryWriter classes to read and write the bytes in the video file.

