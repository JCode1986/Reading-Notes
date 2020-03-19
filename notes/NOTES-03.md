# Reading and Writing Files

## Notes
* Classes fully support inheritance, a fundamental characteristic of object-oriented programming. When you create a class, you can inherit from any other interface or class that is not defined as sealed, and other classes can inherit from your class and override class virtual methods.

* The following example defines a public class that contains an auto-implemented property, a method, and a special method called a constructor. For more information, see Properties, Methods, and Constructors topics. The instances of the class are then instantiated with the new keyword.
```
using System;

public class Person
{
    // Constructor that takes no arguments:
    public Person()
    {
        Name = "unknown";
    }

    // Constructor that takes one argument:
    public Person(string name)
    {
        Name = name;
    }

    // Auto-implemented readonly property:
    public string Name { get; }

    // Method that overrides the base class (System.Object) implementation.
    public override string ToString()
    {
        return Name;
    }
}
class TestPerson
{
    static void Main()
    {
        // Call the constructor that has no parameters.
        var person1 = new Person();
        Console.WriteLine(person1.Name);

        // Call the constructor that has one parameter.
        var person2 = new Person("Sarah Jones");
        Console.WriteLine(person2.Name);
        // Get the string representation of the person2 instance.
        Console.WriteLine(person2);

        Console.WriteLine("Press any key to exit.");
        Console.ReadKey();
    }
}
// Output:
// unknown
// Sarah Jones
// Sarah Jones
```

Resources:
* [Classes](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/classes)
* [Constructors](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/constructors)
* [Properties](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/properties)
* [Stack and Heap](https://www.c-sharpcorner.com/article/C-Sharp-heaping-vs-stacking-in-net-part-i/)
* [Garbage Collection Fundamentals](https://docs.microsoft.com/en-us/dotnet/standard/garbage-collection/fundamentals)

