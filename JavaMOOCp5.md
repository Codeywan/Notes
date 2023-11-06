# More Objects

### Constructor Overloading

A class can have multiple constructors if they differ in the **number** or **type** of their parameters:

```Java
public Person(String name) {
    this.name = name;
    this.age = 0;
    this.weight = 0;
    this.height = 0;
}

public Person(String name, int age) {
    this.name = name;
    this.age = age;
    this.weight = 0;
    this.height = 0;
}
```

You can't also have a constructor that takes name and weight here because weight is an int and int is already being used in a constructor. 

A constructor can call another constructor by using the `this` keyword:

```Java
public Person(String name) {
    this(name, 0);
}

public Person(String name, int age) {
    this.name = name;
    this.age = age;
    this.weight = 0;
    this.height = 0;
}
```
Basically, the first constructor is just using the second constructor and setting the age to 0.
*Constructor calls must be the first command in the constructor

Methods can be overloaded too:

```Java
public void growOlder(int years) {
    this.age = this.age + years;
}

public void growOlder() {
    this.growOlder(1);
}
```

