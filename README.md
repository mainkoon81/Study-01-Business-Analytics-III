# Study-01-Business-Analytics-III

### Intro to Object-Oriented-Programming
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
 - the thing is different kinds of objects have a certain amount in common with each other.
 - What OOP allows us to do is..to create **classes** to inherit commonly used standard behavior from other classes. 
 - First let's imagine the basic CLASS and add some states(fields) and behaviors(methods).
 - Then, let's imagine other CLASSES..If you want to inherit from another class (want to access the **states of behavior** in other classes, ie.. the common class), we use `extends` keyword. Then go to CODE > GENERATE > **constructor** 
 - Then What `super` means ?? 
   - Call the 'constructor' for the CLASS we are extending from..which is, we consider, the 'generic CLASS'.  
 - Now, in this other classes, we can add specific features - extra fields, extra methods...
 - When you are done, write the main class!!!

> 3. BlahBlah
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
   - `Static` methods cannot access **instance methods and variables** directly. They're usually used for **operations that don't require any data from an instance** of the class (sth from `this` which is the current instance of a class). so we cannot use `this` keyword. 
<img src="https://user-images.githubusercontent.com/31917400/45169113-d0eb0580-b1f4-11e8-90ca-59be4996e8eb.jpg" />



 - Static variable VS Instance variable
 
 
 













































































































