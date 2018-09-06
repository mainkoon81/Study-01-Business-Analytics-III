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
 
 - __`this` VS `super` VS `this()` VS `super()`__
<img src="https://user-images.githubusercontent.com/31917400/45154051-1cd68400-b1ce-11e8-9d6b-52742f7bc85f.jpg" />
<img src="https://user-images.githubusercontent.com/31917400/45160043-57491c80-b1e0-11e8-991f-882d4b1afde5.jpg" />
 
 - __Method Overloading VS Overriding__
 
 
 - Static Method VS Instance Method
 
 - Static variable VS Instance variable
 
 
 













































































































