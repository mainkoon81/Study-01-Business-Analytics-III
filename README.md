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
 
> 1> instance variable (object)
```
public class Counter {
      private int **value**;
```      
: it stores the data of a **class_object**.
 - it should always be `private` unless it is a **constant**(generally accepted).
 - Each **class_object** has its own set of instance variables. 
 - How to declare instance variable? :
   - `private`: accessor(modifier)
   - `int`: type declaration
   - `**value**`: object identifier ??????????????????????????????????????????????????????????
   
> 2> constructor (object)
 - It initializes the instance(object) variables.
 - A constructor is also considered as a method, so constructor overloading is allowed. 
 - Constructor name is the class name, and all constructors of a class have the same name(with different parameters).
 - Constructor body is executed when new object is created(initialized).
# When referring to an instance variable in a constructor, the compiler automatically applies it to the `this` reference ?
```
public class Counter {
      // this is the instance variable
      private int **value**;
      
      // writing a constructor, this is called 'public interface'
      public Counter() {
            this.value = 0; }
      public Counter(double init_value) {
            this.value = init_value; }
```
'public interface' specifies what you can do with the objects of a class. The**public constructors and methods** of a class form the public interface of the class. 

> 3> methods 
 - instance variables can only be accessed by **methods** of the same class.
# When you refer to an instance variable in a method, the compiler automatically applies it to the `this` reference ?
```
public class Counter {
      private int **value**;
       
      // writing methods, this is called 'pubic interface'
      public void count() {
            value = value + 1; }
      public void reset() {
            value = 0; }
      public int getValue() {
            return value; }
```








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
 - object value (created by User) can be manipulated by calling **methods** by User, and accessible by object ???: `fun.talk()`???
 - tagged by `static`, it becomes a **class variable** only accessible by **class_name**: `Human.GOD` 
 - Otherwise, it's an **instance variable** accessible by **object**: `man.age`
 - tagged by `final`, the value just **cannot be modified**, and still accessible by **class_name**: `Human.God`
```
public class Human {
     private double fun;                 // fun is an instance variable
     private int age;                    // age is an instance variable 
     public static final int GOD = 0;   // GOD is an class variable
     
     Human man = new Human();           // object 
     Human woman = new Human();         // object
     man.age = 15;                      // age is an instance variable
     woman.age =20;                     // age is an instance variable 
     
     public void talk() {
          fun = fun + 1; }              // fun is an instance variable. talk() is a method.
```

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

> practice: Analyzing an Expression 
```

```

> practice: 'CashRegister.java'
```

```



































































































