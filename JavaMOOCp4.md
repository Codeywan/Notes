# JAVA REFRESHER

Reading input: 

```Java
Scanner scanner = new Scanner(System.in);
String name = scanner.nextLine();

System.out.println("What is your name?");
```

Create new `Scanner` object to read input
Then call `scanner.nextLine()` method to read the next line into the name variable    

##### Read information separated by commas

```Java
System.out.println("Enter information separated by commas");
while(true) {
    System.out.println("Enter info, empty will stop");
    String info = scanner.nextLine();

    if (info.isEmpty()) {
        break;
    }

    String[] pieces = info.split(",");
    String name = pieces[0];
    int age = Integer.valueOf(parts[1]);
    //Create new person object with inputted info and add them to persons list
    persons.add(new Person(name, age));
}
```

1. Read input separated by commas
1. If input is empty, end the loop
1. Split the info into a list of strings
1. The position in the strings list corresponds to the piece of information
1. `Integer.valueOf()` converts the string type input into an integer type




## Classes and Objects

* __Class:__ defines the attributes of objects (The blueprints to build a house). Each class is its own `.java` file
    * __Instance variables:__ each individual attribute of a class
    * __Methods:__ define the functionality of a class    
* __Object:__ An instance of a class (An individual house)<br>


### Methods


##### Constructor

A method that creates an object and sets the default values. Defined in the class.

##### Creating a Class:
        
__Example__:
For a "Person" class, the file would be named `Person.java`

```Java
public class Person {
    private String name;
    private int age;
}
```

The class above has two private variables for a Person object. The instance variables are private to keep from being altered. Called encapsulation

##### Creating a Constructor

```Java
public class Person {
    private String name;
    private int age;

    public Person(String initialName) {
        this.age = 0;
        this.name = initialName;
    }
}
```

In the code above, a Person object would be created if the Person method was called and the inital values would be set to age = 0 and name = initialName
ex:
```Java
Person john = new Person("John");
```
We set a variable `"john"` of the `Person` type to hold an object created by the `Person()` constructor, which took the string `"John"` as an argument

The name of the constructor is always the same as the class name. The constructor method is defined within the class

If constructor is not defined, it usually sets values to null or 0

##### Methods other than the constructor 

```Java
public class Person {
    private String name;
    private int age;

    public Person(String initialName) {
        this.age = 0;
        this.name = initialName;
    }

    public void printPerson() {
        System.out.println(this.name + "is " + this.age + "years old") 
    }
}
```

`printPerson()` is a method that takes no parameters
`public` means it is intended to be visible and accessible from outside this class
`void` means the method does not return a value

`static` modifier means the method does not belong to an object, so it cannot access any variables that belong to an object

`this.age` means "this" object's age instance variable

##### Returning a value with a method

```Java
public class Person {
    private String name;
    private int age;

    public Person(String initialName) {
        this.age = 0;
        this.name = initialName;
    }

    public int getAge() {
         return this.age;
    }
}
```

The above example replaces `void` with `int` and indicates that the method will return an integer. This specific method example is called a "getter" because it "gets" the object age

##### String Representation and toString Method

```Java
public class Person {
    private String name;
    private int age;

    public Person(String initialName) {
        this.age = 0;
        this.name = initialName;
    }

    public int getAge() {
         return this.age;
    }

    public String toString() {
        return this.name + ", age: " + this.age;
    }
}
```

The `toString()` method is the preferred way for defining the string representation of an object. Not using `print` methods in the class

Instead of calling the `toString()` method like `john.toString()` as you would with other methods, it is used like this:

```Java
Person john = new Person("John");

System.out.println(john);
```
Java automatically retreives the string representation by extending the call to function as:
```Java
System.out.println(john.toString());
```

### Obects in Lists

```Java
ArrayList<String> strings = new ArrayList<>();
```
Makes a list to hold strings

```Java
ArrayList<Integer> numbers = new ArrayList<>();
```
Makes a list to hold integers

```Java
ArrayList<Person> people = new ArrayList<>();
```
Makes a list to hold `Person` objects















