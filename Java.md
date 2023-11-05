## Classes and Objects

* __Class:__ defines the attributes of objects (The blueprints to build a house). Each class is its own `.java` file
    * __Instance variables:__ each individual attribute of a class
    * __Methods:__ define the functionality of a class    
* __Object:__ An instance of a class (An individual house)<br>


#### Methods


###### Constructor

A method that creates an object and sets the default values. Defined in the class.

###### Creating a Class:

__Example__:

For a "Person" class, the file would be named `Person.java`

```Java
public class Person {
    private String name;
    private int age;
}
```

The class above has two private variables for a Person object. The instance variables are private to keep from being altered. Called encapsulation

###### Using a Constructor

```Java
public class Person {
    private String name;
    private int age;

    public Person(String initialName) {
        this.age = 0;
        this.name = initialName;
    }

    public void printPerson() {
        System.out.println(this.name + "is " + this.age + "years old") {
    }
}
```

In the code above, a Person object would be created if the Person method was called and the inital values would be set to age = 0 and name = initialName

The name of the constructor is always the same as the class name. The constructor method is defined within the class

If constructor is not defined, it usually sets values to null or 0

###### Methods other than constructor 









