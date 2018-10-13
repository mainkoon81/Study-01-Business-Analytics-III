# Study-01-Business-Analytics-III

### Java Object-Oriented-Programming
> 1. CLASS
 - Two characteristics of the object
   - **state:** head_size? number of legs? wings? ... software object store it in **variable**. 
   - **behavior:** fly? bite? carry? ... softeware object expose it with **methods**.
 - Then what's CLASS ??
   - CLASS is a sort of a **template** or a blueprint for creating **object**.
   - why CLASS? Because..the data_types(float, String,..) are limiting. CLASS could be a powerful **user-defined data_type**, sort of an extra data_type.
 - How to write CLASS?
   - **public**: An "access modifier" to determine **what access** we want to allow others to have to this new class that we're creating...so 'public' means **unrestricted access**.
   - **private**: When talking about variables(fields), an "access modifier"-'private' means, we want "encapsulation"(which is a key fundamental rule of object-orientated programming). So encapsulation in Java is used to hide the fields and methods from access publicly.
   - First, create some variables(fields) that are parts of this CLASS (this takes place in the file different from the main class file). 
   - If you recall, CLASS is just a template. We need to create an object that will take that template. We go back to the **main class**  `class Main()`, create the object name(consider this name as the new user-defined datatype) and say `new` to initialize it. It's like we create the object based on the template 'CLASS'. 

> 2.INHERITANCE
 - The thing is different kinds of objects have a certain amount in common with each other. What OOP allows us to do is..to create **classes** to inherit commonly used standard behavior from other classes. Very simple little example: We have a class 'Vehicle'. and create a class 'Car' extends from 'Vehicle'. Now it's got a relationship with Vehicle. So you can quite correctly say, Car is a Vehicle and that's essentially what inheritance is.
 - First let's imagine the basic CLASS and add some states(fields) and behaviors(methods).
 - Then, let's imagine other CLASSES..If you want to inherit from another class (want to access the **states of behavior** in other classes, ie.. the common class), we use `extends` keyword. Then go to CODE > GENERATE > **constructor** to select inheritable fields..
 - Then What `super()` means ?? 
   - Call the 'constructor' for the CLASS we are extending from..which is, we consider, the 'generic CLASS' or 'parent'. So parent itself is summoned.  
 - Now, in this other classes(the child class), we can add specific features - extra fields, extra methods...
 - When it's done, we can write the main class!!!

> 3. Basic Object Oriented Programming Knowledge
 - __Reference VS Instance(object) VS Class__
   - With an analogy of building a building, 
     - Class: the plan of the building
     - Instance(object): Each building you build(instantiate using the new operator) 
     - Reference: address. We can pass the references as parameters to **'constructors and methods'**. 
<img src="https://user-images.githubusercontent.com/31917400/45151965-9cad2000-b1c7-11e8-9c99-d1304a007734.jpg" />
<img src="https://user-images.githubusercontent.com/31917400/45091507-92791c00-b10a-11e8-942a-ac5e82619a04.jpg" />
 
 - __`this` VS `super` VS `this()` VS `super()`__ 멤버(variable, method) or 통째 
<img src="https://user-images.githubusercontent.com/31917400/45160420-52389d00-b1e1-11e8-8edb-5ea3ffdf6c22.jpg" />
<img src="https://user-images.githubusercontent.com/31917400/45160043-57491c80-b1e0-11e8-991f-882d4b1afde5.jpg" />
 
 - __Method Overloading VS Method Overriding__
   - Method Overloading: providing two or more separate methods **in a class** with the same name but with different parameters. It is handy coz it reduces duplicated code and we don't have to remember multiple method names. It has nothing to do with polymorphism but people refer to overloading as **"compile-time polymorphism"**, so in other words, the compiler decided which method is going to be called based on the 1)method name, 2)return type and 3)argument list. We can overload static and instance methods. Usually overloading happens inside a single class, but a method can also be treated as overloaded in the subclass of that class. 
   - Method Overriding: defining a method in a child class that already present in parent class with same signature(name, arg). By extending the parent class, the child class can get all the methods in the parent. People refer to overriding as **Run-time polymorphism**(Dynamic method dispatch). We can't override **static method** but only **instance method**. 
     - note: constructor and private method cannot be overriden. It uses `super.method()` 
<img src="https://user-images.githubusercontent.com/31917400/45167066-4902fc80-b1f0-11e8-9298-20d4c2778c43.jpg" />

 - __Static Method VS Instance Method__
   - **Static** methods cannot access **instance methods and variables** directly. They're usually used for **operations that don't require any data from an instance** of the class (sth from `this` which is the current instance of a class). so we cannot use `this` keyword.
   - **Instance** methods belong to an instance of a class. To use instance method, we need to **instantiate the class** first by using `new` keyword. Instance methods can access instance methods and variables directly. Instance methods can access static methods and variables directly. 
   - So...when to create **static** method or **instance** method ??
<img src="https://user-images.githubusercontent.com/31917400/45172757-31cb0b80-b1fe-11e8-91da-0d47e70b5481.jpg" />
<img src="https://user-images.githubusercontent.com/31917400/45169113-d0eb0580-b1f4-11e8-90ca-59be4996e8eb.jpg" />
<img src="https://user-images.githubusercontent.com/31917400/45172581-a5204d80-b1fd-11e8-9071-dcebbe924b9f.jpg" />
 
 - __Static(member) variable VS Instance variable__
   - **Static** variables are declared by keyword `static`. Every instance of that class **shares** the same static variable. If changes are made to that variable, all other instances will see the effect. 
     - For example, when Reading "user_input", using `scanner`, we declare `scanner` as a static variable.
   - **Instance** variables belong to an instance of a class. 
     - every instance has its own copy of an instance variable. 
     - every instance can have a different value(state) and Instance variables represent the state of an instance. 
<img src="https://user-images.githubusercontent.com/31917400/45174955-0cd99700-b204-11e8-8dc5-a7328f63fc40.jpg" />
<img src="https://user-images.githubusercontent.com/31917400/45174959-0fd48780-b204-11e8-998d-290c7b9674ee.jpg" />

> 4. Three components (Composition, Encapsulation, Polymorphism)

__Composition__: Let's look at the scenario of a computer. So our computer has a motherboard, a case, and a monitor but they are not computers in the same sense that a Car is a Vehicle(inheritance). But a computer has a motherboard, a computer has a case, and a computer has a monitor. So that's what composition is, is actually modeling "parts", if you will, "parts" of the **greater whole**.
 - **the obvious advantage here, is that if you're using the `extends` option to inherit, you can only, in Java, inherit from one class at a time, but here, we can access multiple classes at one go.**
 
__Encapsulation__: Encapsulation is the mechanism that allows you to **restrict access** to certain components in the objects that you are creating (you're able to protect the members of a class from external access in order to guard against unauthorized access). It can be very useful to hide that **inner working** from another class to give you more control and to enable you to change things without breaking code elsewhere. 

__Polymorphism__: Polymorphism is the mechanism that allows actions to act differently based on the actual object that the action is being performed on. For example, what's happening is, with that one line of code in `public static void main(String[] args) {...`,   which is `movie.plot()` (and all object are inherited from the base `movie` class) yields different outputs by actually assigning different functionality, depending on the type of object that we've created. you can see how polymorphism works now: It will automatically, if you're inheriting from another class, and you've got a method, and you override that method, that's what polymorphism is. 

### Inner Class VS Abstract Class VS Interface
> 1. Interface
 - ??????? 



################################################################################################################
## [concept]

__# What is **class**?__
 - objects
 - methods
> Entity that contains objects and methods. Class determines legal methods. Class declares the methods that you can apply to its objects. For example, `PrintStream` class allows `System.out` object to `println(), or print(), etc`. `Class is a type.`

> **Overloaded method**: when a class declares multiple methods with the same name, but different parameters. 
 
__# What is **type**?__
 - primitive type
 - class_object type
> Type define **values** or **class_object**(operation) that would be carried out on the values. Note that `int, double, long, String, PrintStream, etc...` those types also have their own **classes** such as `Integer, Double, Long, String, PrintStream, etc...`. 

> pure numbers(int, double, long, etc) are not **class_object** but **primitive** types. 
```
int num = 19;  // 'num' is not an object.
```

__# What is **object**?__
> Entity that should be manipulated by calling methods.

> Each object belongs to a class. For example, the object `System.out` belongs to a class called PrintStream. This is an object that belongs to a class called 'String'.
```
String name = "Minkun";  // 'name' object belongs to 'Sting' class.
```
> there is a particular way to create an object. This is actually `String name = new String("Minkun");` under the hood..

__# What is **writing a variable**?__
 - 1) Declaration 
 - 2) Initialization
 - When we write a variable, we need to take these 2 steps. Plus, we need the name of `variable` or `method` or `object` or `class`: **identifier**
 - then method is a variable?????????????????????????????????????????????
 - then object(instance) is a variable????????????????????????????????????????????????????
 - then class_object is a variable?????????????????????????????????????????????????? 

> so...It is an error to use an identifier that has never had a value assigned to it.
```
int height;      
width = height;  // ERROR—uninitialized variable height!! 
```

__# How to create an object?__
```
Rectangle box = new Rectangle(5, 10, 20, 30);
Rectangle box = new Rectangle();
```
 - `type + obj_identifier = referencing_keyword + constructor(param);`
 - 1) Assumming there is already a class called 'Rectangle' somewhere? 
 - 2) It uses the parameters (in this case, 5, 10, 20, and 30) to **initialize** the data of the **object** which would be one of the many, many objects that can be born from the class called 'Rectangle'.
   - **An object is an instance.** And this instance is called 'box'. 
   - then basic method for 'box' example:
     - `double width = box.getWidth()` ?
     - `double height = box.getHeight()` ?
 - 3) **Object** reference: 
   - The `new` keyword returns a reference(location) to a new object. 
   - **Multiple object variables can refer to the same object**: 
     - Here 'box' is just an **address**, thus the change in box2 will change the object box as well. 
   - However, Note: Primitive type variables ≠ object variables      
```
Rectangle box1 = new Rectangle(5, 10, 20, 30);  // object variable   
Rectangle box2 = box;     
box2.translate(15, 25);                         // 'box1' value has changed
    
int number_1 = 50;                              // primitive type variable
int number_2 = number_1;
int number_2 = 80;                              // 'number_1' value does not change
```

__# What is **API** documentation?__
> API documentation lists **classes and methods** in the Java library. The detailed description of a method shows:  
 - The action that the method carries out 
 - The parameters that the method receives 
 - The value that it returns (or the reserved word void if the method doesn’t return any value) 
 - Package: a collection of classes with a related purpose

# ok
__how to declare a class?__ let's create a class_object...

## it's all about differentiating the `property`, `functionality` b/w Queen(class) and nymphs(objects)
 - private, public, static, final...
 
> __1> instance variable__ (is it an object?)
```
public class Counter {
      // this is the instance variable. It's a property of the baby objects.
      private int **eye**;
```      
: instance_variables store the data of a **class_object**.
 - instance_variable should always be `private` unless it is a **constant**(generally accepted).
 - Each **class_object** has its own set of instance variables. 
 - How to declare instance variable? :
   - `private`: accessor(modifier)
   - `int`: type declaration
   - `**eye**`: object_property. It will be called when `object_identifier.eye`
   
> __2> constructor__ (method)
 - It initializes the instance variables.
 - A constructor is also considered as a method, so constructor overloading is allowed. 
 - Constructor name is the class name, and all constructors of a class have the same name(with different parameters).
 - Constructor body is executed when new object is created(initialized) in the `Main.java`.
```
public class Counter {
      private int **eye**;
      
      // writing a constructor, this is called 'public interface'
      // 'this' referring the object identifiersss that will be generated in the Main.java in the future.
      public Counter() {
            this.eye = 0; }
      public Counter(double init_eye) {
            this.eye = init_eye; }
```
'public interface' specifies what you can do with the objects of a class. The **public constructors and methods** of a class form the public interface of the class. 

> 3> methods 
 - **instance variables** can only be accessed by **methods** of the same class.
 - When you refer to an instance variable in a method, the compiler automatically applies it to the `this` reference ?
```
public class Counter {
      private int **eye**;
      public Counter() {
            this.eye = 0; }
      public Counter(double init_eye) {
            this.eye = init_eye; }
            
      // writing methods, this is called 'pubic interface'
      public void count() {
            eye = eye + 1; } //no return, but execute
      public void reset() {
            eye = 0; }       //no return, bur execute
      public int getEye() {
            return eye; }    //return sth
```
<img src="https://user-images.githubusercontent.com/31917400/45927098-9f2cab00-bf25-11e8-993f-0f3578cefb98.jpg" />

### Data types
> What is a constant? 
 - `final` variable. Once its value has been set, it cannot be changed. 
 - Convention: Use all-uppercase names for constants... 
 - If constant values are needed in several methods, tag them as `static` and `final`.
```
public class Math {
      public static final double PI = 3.14159265358979323846;
```
> **object value** and `static`and `final`
 - __accessible by what?__ 
 - object value (created by User by initialization) can be manipulated by calling **methods** by User, and accessible by object.
 - tagged by `static`, it becomes a **class variable** only accessible by **class_name**: `Human.GOD` 
 - Otherwise, it's an **instance variable** accessible by **object**: `man.age`
 - tagged by `final`, the value just **cannot be modified**, and still accessible by **class_name**: `Human.God` coz it's a static(class) constant variable just like `Math.PI` which is 3.14
```
public class Human {
     private double fun;                 // fun is an instance variable
     private int age;                    // age is an instance variable 
     public static final int GOD = 0;   // GOD is an class(static) constant variable
     
     Human man = new Human();           // object 
     Human woman = new Human();         // object
     man.age = 15;                      // age is an instance variable
     woman.age =20;                     // age is an instance variable 
     
     public void talk() {
          fun = fun + 1; }              // fun is an instance variable. talk() is a method.
```
> Class Method example(class.method)
 - Convert string to number: `Integer.parseInt(input)`, `Double.parseDouble(input)`
 - Convert number to string: `String blah = "" + input;`, `blah = Integer.toString(input)`???

> increment & decrement 
 - The idea is that `++i` increments i and **returns that value**, while `i++` **returns i's value first** and then increments i.
```
int i = 0;
int j = i++;
int k = ++i;
System.out.println(i);  //? 2
System.out.println(j);  //? 0
System.out.println(k);  //? 2
```

### Array
`int[] IntArray = new int[length];` `String[][] board = new String[ROWS][COLUMNS];` When we create an primitive type integer values such as `int x` and `int y`, taking up 4byte each, our OS randomly selects the location of the memory spaces while we create an array, every values belongs to `int[] x` are stored consecutively one after another. That's why our array entities need to have a consistent type(because of `char: 2byte, int: 4byte, double: 8byte`). Plus, it is a good idea to use a named constant. 
```
final int myLength = 10;
int[] IntArray = new int[myLength];
```
<img src="https://user-images.githubusercontent.com/31917400/46072374-1e1a2180-c17a-11e8-9785-732a4c82084d.jpg" />

> Do not reorganize Parallel arrays(two arrays with different type) into an array of objects. Look at this mapping case.
```
String[] cities = {"Dublin", "London", "Paris"};
int[] population = {4, 8, 6];
for (int i=0; i<cities.length; i++) {
   System.out.println(cities[i] + "=" + population[i]; }
```
Dublin=4, London=8, Paris=6 ? Nope!!!! What if the value changes? That's why.. 
## we need to create **class object**. 
```
public class City {
    //introduce properties
    private String name;
    private int population;

    //constructor
    public City(String name, int population){
        this.name = name;
        this.population = population;
    }

    //method
    public String showName(){
        return this.name;
    }
    public int showNum(){
        return this.population;
    }

}
##############################################################################################
import java.util.Arrays;

public class Main {

    public static void main(String[] args) {
        City city_1 = new City("Dublin", 4); //this is what we want: object
        City city_2 = new City("London", 8); //this is what we want: object
        City city_3 = new City("Paris", 6); //this is what we want: object

        //u know what?  cannot access property : city_1.name; meh meh..that's why we need methods
        System.out.println(city_1.showName());

        //make a custom class arrays wow....
        City[] cities = new City[3]; //initialization
        cities[0] = city_1; //store the object
        cities[1] = city_2; //store the object
        cities[2] = city_3; //store the object

        for(int i=0; i<cities.length; i++) {
            System.out.print(cities[i].showName() + ", " + cities[i].showNum() + " / ");
        }
```
Dublin, 4 / London, 8 / Paris, 6 /

### Arraylist<Class>
`ArrayList<type> identifier = new ArrayList<type>();` 

ArrayList is also array, but special array...Compare: 
 - array:`int[] meh = new int[length]`..no need to say it's an array. 
 - array_list:`ArrayList<Integer> meh = new ArrayList<Integer>();`..it's special so say **ArrayList**.

__So Why ArrayList<Class>?__: type and length
 - 1) Stricktly `typed`: the entity types should be consistent
   - Solution: make a `custumized class` to create an independent array object.`ArrayList<Minkun> you = new ArratList<Minkun>();`
   - so..each entity in an array is an **object** born from the class called `Minkun`!!!! so any objects can go.
 - 2) fixed `length`: what if we don't know how many entities will be stored in the array?
   - Solution: **ArrayList**. Arraylist Can grow and shrink as needed! 
 - 3) **ArrayList class** supplies methods for many common tasks, such as `object.size()`, inserting:`object.add(index, "sth")`, `object.remove(index)`, replacing:`object.set(index, "sth")`, `object.get(index)`, etc. Here, object is each element of our ArrayList!
 - 4) auto-boxing?
   - `int x = 5;`: x is not an object. It's a variable. 
   - `Integer x = new Integer(5);`: x is an object. To treat `primitive_type values` as objects, you must use **wrapper_classes**. In Java, conversion between `primitive_types` and the corresponding **wrapper_classes** is automatic. This process is called **auto-boxing** (even though **auto-wrapping** would've been more consistent). 
   - FYI, Remember to use the **wrapper_type** when you declare the **ArrayList**, and then rely on auto-boxing.
 
```
ArrayList<Double> doublesss = new ArrayList<Double>(); 
doublesss.add(29.95); 
double x = doublesss.get(0);`
```
```
public class BankAccount {
    //instance variables
    private int accountNum;
    private double balance;

    //Construct a bank account with a zero balance
    public BankAccount(int anAccountNumber) {
        this.accountNum = anAccountNumber;
        this.balance = 0;
    }

    //constructor overloading
    //Constructs a bank account with a given balance
    public BankAccount(int anAccountNumber, double initialBalance) {
        this.accountNum = anAccountNumber;
        this.balance = initialBalance;
    }

    //methods
    //Gets the account number of this bank account
    public int getAccountNum() {
        return this.accountNum;
    }
    //Deposits money into the bank account.
    public void deposit(double amount) {
        this.balance = this.balance + amount;
    }
    //Withdraws money from the bank account.
    public void withdraw(double amount) {
        this.balance = this.balance - amount;
    }
    //Gets the current balance of the bank account.
    public double getBalance() {
        return this.balance;
    }
}

##############################################################################################
public class Main {
    public static void main(String[] args) {
        //empty arraylist
        ArrayList<BankAccount> superAccount = new ArrayList<BankAccount>();
        
        //add the object
        BankAccount you = new BankAccount(1001);
        superAccount.add(you);
        BankAccount me = new BankAccount(1015);
        superAccount.add(me);
        superAccount.remove(0);

        System.out.println("Size: " + (superAccount.size()));
        System.out.println(superAccount.get(1).getAccountNum());
```
> To collect numbers(with primitive types) in an array list, we use the wrapper type(`Integer`, `Double`, etc) as the type parameter, but storing wrapped numbers is quite inefficient..coz each number is a big object. 

### Common Array Algorithm
> Filling (arraylist)
 - Fill an array with zeroes then fill an array-list with squares
```
ArrayList<Integer> arrLt = new ArrayList<Integer>(); //object
arrLt.add(0, 45); arrLt.add(1, 25); arrLt.add(2, 38); 
for(int i=0; i<arrLt.size(); i++) { 
    arrLt.set(i, i*i); }
```
> Sum and AVG (arraylist)
 -  compute the sum of all elements for array-list and obtain AVG
```
double total = 0;
for(i : arrLt) {
    total += i; }
double AVG = total / arrLt.size();
```
> Counting matches (arrayList)
 - Count the number of accounts whose balance is at least as much as a **given threshold**
```
public class Bank {    
    private ArrayList<BankAccount> arrLt; 
    
    public int count(double atLeast){
        int matches = 0;       
        for (BankAccount i : arrLt){          
            if(i.getBalance() >= atLeast){
                matches++; } 
        } //????
        return matches; }
    }
```
> Max and Min
 -  Find the account with the largest balance in the bank
```
BankAccount WhatMax = arrLt.get(0); //initialize a candidate

for(int i=1; i<arrLt.size(); i++) {
    BankAccount a = arrLt.get(i);
    if(a.getBalance() > WhatMax.getBalance){
        WhatMax = a; } 
}
```
> Searching
 -  Determine whether there is a bank account with a particular account number in the bank..**Writing a new class?**
```
public class Bank(int account_number) {
    for(BankAccount i : arrLt){
        if(i.getAccountNumber()==account_number){
            return i; }
    return null; }
    .
    .
```
> Locating
 - Find the position of an element so that you can replace or remove it. Find the position of the first element that is larger than 100.
```
int position = 0;
boolean found = false;
while(position < arrLt.size() && !found) {
    if(arrLt.get(position)>100){
        found = true; }
    else {position++; }
```
> Removing, Inserting

> Copying an Array

> Growing an Array

> Printing "|" separators

### Interface for algorithm reuse
<img src="https://user-images.githubusercontent.com/31917400/46256117-4bc6d980-c49e-11e8-9236-f70a9be5f527.jpg" />

## So what's the story?
__Rule:__ We want to recycle the algorithm. What we need are `1)class file, 2)interface file, 3)algorithm file, 4)Main file`. How `factories(classes)` interact with the `Ship(the target algorithm)`? **We might need a `port(the interface file)`**.
 
> Q. Then where do we write the implementation of the new method(algorithm)? (in the algorithm class?). To utilize the algorithm, we need to create `interface_type` objects. Where is our `interface_type` objects created and initialized? (in Main.java file?) And where is our `interface_type` object(replacing all kinds of other class_type objects) utilized? (in Main.java file?). 
 
 > In the Class files(factories)
 - Here, we design a queen's womb for procreating objects(instance variables(object), constructors(method), instance methods(method)), and queen's body that consists of objects and methods(static variables, static methods). Eventually, in the Main file, queen's objects will be initialized. When it comes to the all methods in the class files, they provide information about objects(baby: incomplete, individual properties) and class_objects(queen: complete, shared, fixed properties, or constants). If we want to make comparison between objects, or to create sth, using objects, we should write method_implementation in the Main file. 
 
> In the 'Main.java'
 - Technically, it's a class file.
 - In the Main file, let's say, we found that different classes gave birth to different groups of objects then they are contributing to creating sth, but these creations are sharing the same algorithm.  
<img src="https://user-images.githubusercontent.com/31917400/46251420-f9f46400-c449-11e8-8aa9-abcf81801f33.jpg" />

## In this case, we throw away these methods from this Main file. Instead, we create **new algorithm file separately** and write a single method implementation (need to be hinted at by **interface file**) in the algorithm file.    

> In the Interface file(a port) 
 - Technically, it's an interface file. 
 - It is simply saying like `"Hey, to use our master algorithm, our all object_types will be replaced with this one **single interface_type** and its interface object method will be newly-added and implemented in each class file, then the history would happen in the algorithm file."` 
 - A Java interface is a bit like a class, except it can only contain **method signatures**(headers, name, parameters and exceptions) and **fields** without implementation(that's why it's an **abstract method**). We'll call this interface file 'Measurable' and write a method(algorithm) signature.  
 - All methods in an interface are public(so automatically public).
```
public interface Measurable { 
    //method signature
    public double getMeasure();  }
```

> In the Algorithm file(a ship)
 - Technically, it's also a class file. 
 - The implementation starts here. Now that we have an interface type that denotes measurability, we can implement a reusable algorithm(method). This method is useful for objects of any class that conforms to the Measurable interface(type). 
 - How this file connects to the interface file? The algorithm method uses the `interface_object's name` as its parameter and the `interface_ method's name` as the interface_object's method. We removed lots of methods in the Main file. Here, we conjure them with using a single method...POLYMORPHISM.
 - In this example, the algorithm takes an array object that has the interface type.   
```
public class AVG {
    // algorithm signature and implementation
    public static double average(Measurable[] objects){
        double sum = 0;
        for(Measurable i : objects){
            sum = sum + i.getMeasure(); //Here, we r using 'getMeasure()' we registered in the interface file. 
        }
        if(objects.length>0) {return sum/objects.length;}
        else {return 0;}
    }
}
```

> Back to the class files(factories)
 - What do we need to change? - 1)header, 2)adding the abstract method(Not denoting the algorithm, but the interface's method).
```
public class BankAccount implements Measurable {
    ......
    ......
    public double getMeasure(){
        return this.balance;
    }
}
```
```
public class Country implements Measurable {
    ......
    ......
    public double getMeasure(){
        return this.area;
    }
}
```

> Back to the Main file
 - What do we need to add? - initializing 'Measurable' objects. 
```
public class Main {
    public static void main(String[] args) {
        ......
        ......
        // objects
        BankAccount[] objects = new BankAccount[3];
        objects[0] = new BankAccount(11223344, 1000);
        objects[1] = new BankAccount(66553343, 2345);
        objects[2] = new BankAccount(66553345, 21313);
        
        // interface_type objects
        Measurable[] objs = new Measurable[3];
        objs[0] = new BankAccount(11223344, 1000);
        objs[1] = new BankAccount(66553343, 2345);
        objs[2] = new BankAccount(66553345, 21313);
        System.out.println(AVG.average(objs)); // This is the moment we use the algorithm
        
        // objects
        Country[] countries = new Country[3];
        countries[0] = new Country("Ireland", 50);
        countries[1] = new Country("Korea", 100);
        countries[2] = new Country("India", 120);
        
        // interface_type objects
        Measurable[] ctr = new Measurable[3];
        ctr[0] = new Country("Ireland", 50);
        ctr[1] = new Country("Korea", 100);
        ctr[2] = new Country("India", 120);
        System.out.println(AVG.average(ctr)); // This is the moment we use the algorithm
```

### Exception Handling
There are two aspects to dealing with **program errors** `detection` and `handling`. In Java, exception handling provides a flexible mechanism for passing control from the point of error detection to a handler that can deal with the error. 
> **Throwing Exceptions**
 - When you detect an error condition, your job is really easy: **Throw an appropriate **exception_object**!**. For example,  
```
if (amount > balance) { // Now what? }
```
 - First look for an appropriate **exception_class**. The Java library provides many classes to signal all sorts of exceptional conditions. 
 - Seemingly, Is it an `arithmetic error` to have a negative balance? Nope! Java can deal with negative numbers. Is the amount to be withdrawn illegal? Indeed it is. It is just too large. Therefore, let’s throw an `IllegalArgument Exception`. To signal an exceptional condition, use the `throw` statement to throw an **exception object**!  
<img src="https://user-images.githubusercontent.com/31917400/46554141-3f47e400-c8d7-11e8-8014-50ce7fc828ec.jpg" />

 - When you throw an exception, execution does not continue with the next statement but with an **exception handler** ONLY.

> **Catching Exception**
 - Every exception should be handled somewhere in your program. If an exception has no handler, an **error message is printed, and your program terminates**. You can handle exceptions with the **`try/catch` statement**. Place the statement into a location of your program that knows how to handle a particular exception. 
 - The `try` block contains one or more statements that may **cause an exception** of the kind that you are willing to handle. 
 - Each `catch` clause contains the **handler for an exception type**.
```
try {
    statement...
    statement...
    ...
}
catch(Exception_Class Exception_Object) {
    statement...
    statement...
    ...
}    
```
Let's say, 
```
import java.util.Scanner;
 
class Division {
  public static void main(String[] args) {
  int a, b, result;
  Scanner input = new Scanner(System.in);
  System.out.println("Input two integers");
  a = input.nextInt();
  b = input.nextInt();
  
  result = a / b;
  System.out.println("Result = " + result);
  }
}
```
but we cannot divide by zero. so we get..
<img src="https://user-images.githubusercontent.com/31917400/46554936-bed6b280-c8d9-11e8-90bb-ba83abc1e6ea.png" />

Now, it's time to use `try` and `catch`!!
```
class Division {
  public static void main(String[] args) {
  int a, b, result;
  Scanner input = new Scanner(System.in);
  System.out.println("Input two integers");
  a = input.nextInt();
  b = input.nextInt();
 
  // try block
  try {
    result  = a / b;
    System.out.println("Result = " + result); }
 
  // catch block
  catch (ArithmeticException e) {
    System.out.println("Exception caught: Division by zero."); }
  }
}
```
 - Whenever an exception is caught corresponding `catch` block is executed, For example, this program catches `ArithmeticException` only. If some other kind of exception is thrown it will not be caught so it's the programmer work to take care of all the exceptions. As in our `try` block, **we are performing arithmetic so we are capturing only arithmetic exceptions**. 
 - Use an object of Exception class as other classes inherit Exception class. 
```
class Exceptions {
  public static void main(String[] args) {
  String languages[] = { "C", "C++", "Java", "Perl", "Python" };
       
  try {
    for (int c = 1; c <= 5; c++) {
      System.out.println(languages[c]); }
  }
  catch (Exception e) {
    System.out.println(e); }
  }
}
```
output: 
 - C++
 - Java
 - Perl
 - Python
 - **java.lang.ArrayIndexOutOfBoundsException: 5**

Here our catch block captures an exception which occurs because we are trying to access an array element which does not exist. Once an exception is thrown control comes out of try block and remaining instructions of try block will not be executed. At compilation time syntax and semantics checking is done and code isn't executed on machine so exceptions can only be detected at run time.

> **Checked Exception**
 - The exceptions that you can throw and catch fall into three categories.
   - 1)`Internal errors` are reported by descendants of the type Error. One example is the **OutOfMemoryError**, which is thrown when all available computer memory has been used up. These are fatal errors that happen rarely. 
   - 2)Descendants of RuntimeException, such as as **IndexOutOfBoundsException** or **IllegalArgumentException** indicate errors in your code. They are called `unchecked exceptions`.
   - 3)All other exceptions are `checked exceptions`. These exceptions indicate that something has gone wrong for some external reason beyond your control. 

-------------------------------------------------------------------------------------------------------
# Java Generics & Collections
## [Intro]
Generics and collections work well. As we shall see, combining them is synergistic: the whole is greater than the sum of its parts. 
> Q. Put three integers into a list(collection?) and add them together. 
 - meh...using an array.
```
int[] intsss = new int[] {1, 2, 3}; 

int sum = 0; 
for(int i = 0; i < intsss.length; i++) { sum += intsss[i]; } 
assert sum == 6;
``` 
 - Here is how to do the same thing with generics: the interface `List` and the class `Arrays` are part of the **Collections Framework**(both are found in the package `java.util`). The type `List` is now generic; you write `List<E>` to indicate a list with elements of type E. And as you expect, any type goes!  
## what is collections ????? why List can be Arrays???
```
List<Integer> intsss = Arrays.aslist(1,2,3);

int sum = 0;
for(int n : intsss) { sum += n; }
assert sum == 6;
```
## damn, where is `new`? where does `Arrays` come from???????????
 - >In the Java Generics, `Boxing` and `Unboxing` operations, used to convert from the primitive type to the wrapper class, are automatically inserted. ??????????????????? (in ordinary java, it ain't work?)
 - >The static method `asList()` takes any number of arguments, places them into an array, and returns a new list backed by the array. ??????????????????
## - >Collections let you easily grow or shrink the size of the collection, or switch to a different representation when appropriate, such as `linked list` or `hash_table` or `ordered_tree`. The introduction of generics, boxing and unboxing, foreach loops, and varargs in Java marks the first time that using collections is just as simple, perhaps even simpler, than using arrays.????????????? 

--------------------------------------------------------------------------------------------------------
## [Generics]
 - We can replace the **parameters** that we declared from the method. Generics allow us to create **class's interface** of the methods that takes the parameters called `type-parameters`. An **interface** or **class** maybe declared to take one or more `type parameters`, which are written in `<class>` angle brackets and should be supplied when you 1)**declare a variable** belonging to the interface or class or when you 2)**create a new instance** of a class.?????????????????????????????
 - In the **Collections_Framework**, class `ArrayList<E>` implements interface `List<E>`. 
## This declares the variable `words` to contain a `list of strings`, and ***creates an "instance" of an ArrayList***: ???????
```
List<String> words = new ArrayList<String>();

words.add("Hello-");
words.add("world");
String s = words.get(0) + words.get(1);
assert s.equals("Hello-world");
```
 - In Java before generics, the same code would be written as:
## whattttttt? ArrayList? List? where is <> ??????????????????????
 - Without generics, the type parameters are omitted, but you must explicitly cast whenever an element is extracted from the list.
 - We say that generics are implemented by erasure because the types `List<Integer>`, `List<String>`, and `List<List<String>>` are all represented at run-time by the same type, `List`. We also use `erasure` to describe the process that converts the first program to the second??????????????????the process erases type parameters but adds casts. 
```
List words = new ArrayList(); 
words.add("Hello-"); 
words.add("world"); 
String s = ((String)words.get(0))+((String)words.get(1)) 
assert s.equals("Hello-world");
```
 - Another consequence of implementing generics by erasure is that array types differ in key ways from parameterized types. Executing a string array `new String[length]` allocates an [array], and stores in that array an indication that its components are of type String. In contrast, executing an ArrayList of String `new ArrayList<String>()` allocates a [list], but does not store in the list **any indication of the type of its elements**. ?????????????????
 - Generics in Java resemble templates in C++. There are just two important things to bear in mind about the relationship between Java generics and C++ templates: `syntax` and `semantics`. The syntax is deliberately similar and the semantics are deliberately different.
 - Syntactically, angle brackets`<>` were chosen because they are familiar to C++ users, and because square brackets would be hard to parse. However, there is one difference in syntax. In C++, nested parameters require extra spaces, so you see things like this: `List< List<String> >`. ????????????????????????
 - Semantically, Java generics are defined by `erasure`, whereas C++ templates are defined by `expansion`. ??????????????????

 - Conversion of a primitive type to the corresponding reference type is called boxing and conversion of the reference type to the corresponding primitive type is called unboxing. 

## [Generic methods & Var-args]
Here is a method that accepts an array of any type and converts it to a list:
```
class Lists {  
   public static <T> List<T> toList(T[] arr) {    
      List<T> list = new ArrayList<T>();    
      for (T elt : arr) { list.add(elt); }    
      return list;  
   }
}
```
Our static method `toList` accepts an array of type `T[]` and returns a list of type `List<T>`, and does so for any type `T`, `which is indicated by writing <T> at the beginning of the method signature, which declares T as a new type variable`. A method which declares a type variable in this way is called a generic method. The method may be invoked as follows:
```
List<Integer> ints = Lists.toList(new Integer[] { 1, 2, 3 }); // here, boxing converts 1, 2, 3 from `int` to `Integer`. 
List<String> words = Lists.toList(new String[] { "hello", "world" });
```



Packing the arguments into an array is cumbersome. The `vararg feature` permits a special, more convenient syntax for the case in which the **last argument of a method is an array**. To use this feature, we replace `T[]` with `T…` in the method declaration: 
```
class Lists {  
   public static <T> List<T> toList(T... arr) {    
      List<T> list = new ArrayList<T>();    
      for (T elt : arr) { list.add(elt); }    
      return list;  
   }
}
```
Now the method may be invoked as follows:
```
List<Integer> ints = Lists.toList(1, 2, 3); 
List<String> words = Lists.toList("hello", "world");
```
 - In this examples, the **type_parameter** to the generic method is inferred, but it may also be given explicitly: `List<Integer> ints = Lists.<Integer>toList();` and `List<Object> objs = Lists.<Object>toList(1, "two", "hello");`
 - In general, the following rule of thumb suffices: in a call to a generic method, if there are one or more arguments that correspond to a type parameter and they all have the same type then the type parameter may be inferred; if there are no arguments that correspond to the type parameter or the arguments belong to different subtypes of the intended type then the type parameter must be given explicitly.?????????????????????????
 
Any number of arguments may precede a last vararg argument. Here is a method that accepts a list and adds all the additional arguments to the end of the list: 
```
class Lists {  
   public static <T> void addAll(List<T> list, T... arr) {  
      for (T elt : arr) { list.add(elt); }
      .....
      ...
```
Whenever a `vararg` is declared, one may either pass a list of arguments to be implicitly packed into an array, or explicitly pass the array directly. Thus, the preceding method may be invoked as follows: 
```
List<Integer> ints = new ArrayList<Integer>(); 
Lists.addAll(ints, 1, 2); 
Lists.addAll(ints, new Integer[] { 3, 4 }); 

assert ints.toString().equals("[1, 2, 3, 4]");
```
Since `varargs` **always create an array**, they should be used only when the argument does not have a generic type.???????














































































