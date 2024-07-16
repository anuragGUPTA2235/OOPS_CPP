# OOPS_CPP
OOPS stands for Object-Oriented Programming System. It is a programming paradigm that uses "objects" to design software. An object is an instance of a class, and a class can be thought of as a blueprint for creating objects. OOPS is widely used in many programming languages such as Java, C++, Python, and more.
# API_E
1. Class and Object
Class: A class is a blueprint or prototype that defines the variables and the methods (functions) common to all objects of a certain kind.
Object: An instance of a class. When a class is defined, no memory is allocated until an object of that class is created.
2. Encapsulation
Encapsulation is the concept of wrapping data (variables) and code (methods) together as a single unit. It restricts direct access to some of an object's components, which can prevent the accidental modification of data. This is achieved through access specifiers like private, protected, and public.
3. Inheritance
Inheritance is the mechanism by which one class (child/subclass) can inherit the properties and methods of another class (parent/superclass). It allows for code reusability and the creation of a hierarchical relationship between classes.
4. Polymorphism
Polymorphism allows methods to do different things based on the object it is acting upon. It can be achieved through method overloading (same method name with different parameters) and method overriding (subclass has a specific implementation of a method that is already defined in its superclass).
5. Abstraction
Abstraction is the concept of hiding the complex implementation details and showing only the essential features of the object. This is done using abstract classes and interfaces in languages like Java.
Object-Oriented Programming System (OOPS) offers several advantages and disadvantages. Understanding both can help in determining when and how to use OOPS effectively.
# OOPS IS BEAUTIFUL
### Advantages of OOPS

1. **Modularity**:
   - **Description**: OOPS allows for the modularization of code, meaning that the code is divided into discrete objects, each representing a part of the application.
   - **Benefit**: This makes the code easier to understand, manage, and debug.

2. **Reusability**:
   - **Description**: Objects and classes can be reused across programs.
   - **Benefit**: Inheritance and polymorphism promote code reuse, reducing redundancy and improving maintainability.

3. **Scalability and Maintainability**:
   - **Description**: OOPS principles like encapsulation and abstraction ensure that code is organized and modular.
   - **Benefit**: This makes it easier to manage and scale large codebases, as changes to one part of the system have minimal impact on others.

4. **Improved Productivity**:
   - **Description**: OOPS enables developers to reuse existing code and create modular components.
   - **Benefit**: This can significantly reduce development time and effort.

5. **Flexibility through Polymorphism**:
   - **Description**: Polymorphism allows methods to operate differently based on the object they are acting on.
   - **Benefit**: This provides flexibility in code design and usage, allowing for more generic and adaptable code.

6. **Effective Problem Solving**:
   - **Description**: OOPS models real-world entities as objects.
   - **Benefit**: This natural mapping makes it easier to solve complex problems and design software systems.

### Disadvantages of OOPS

1. **Increased Complexity**:
   - **Description**: The use of objects, classes, inheritance, and other OOPS concepts can add a layer of complexity.
   - **Drawback**: This can make the learning curve steep for new developers and complicate simple applications.

2. **Performance Overhead**:
   - **Description**: OOPS can introduce additional layers of abstraction, which may lead to performance overhead.
   - **Drawback**: This can be a concern in performance-critical applications, where low-level programming might be more efficient.

3. **Larger Program Size**:
   - **Description**: The modular nature of OOPS often results in larger codebases due to additional classes and objects.
   - **Drawback**: This can lead to increased memory usage and longer compile times.

4. **Steeper Learning Curve**:
   - **Description**: OOPS requires a solid understanding of its principles and concepts.
   - **Drawback**: This can be challenging for beginners and may require more training and practice.

5. **Difficulty in Mapping to Real-World Scenarios**:
   - **Description**: Sometimes, complex real-world relationships and interactions are hard to model accurately using OOPS.
   - **Drawback**: This can lead to over-engineering or inappropriate use of OOPS principles, making the system harder to manage.

6. **Inheritance Issues**:
   - **Description**: Improper use of inheritance can lead to problems like tight coupling and fragile base class issues.
   - **Drawback**: This can make the code harder to maintain and evolve.

### When to Use OOPS

OOPS is particularly beneficial in the following scenarios:
- Large and complex projects where modularity and maintainability are crucial.
- Applications requiring frequent updates and maintenance.
- Projects that involve multiple developers working on different components.
- Systems that model real-world entities and relationships.

### When to Avoid OOPS

OOPS may not be the best choice for:
- Small, simple applications where procedural programming may be more straightforward.
- Performance-critical applications where the overhead of object-oriented features is not acceptable.
- Situations where the additional complexity of OOPS does not justify its benefits.

By weighing these advantages and disadvantages, developers can make informed decisions about when and how to use OOPS to best meet their project's needs.
# ACCESS MODIFIERS
![image](https://github.com/user-attachments/assets/9736d5b9-6780-42c9-9787-c91e31e28e8d)
# CLASS OBJECT ATTRIBUTES METHODS ACCESS MODIFIERS
```
#include<iostream>
#include<string>
using namespace std;

class Teacher{
    public:   // access modifiers
    // attributes
int srn;
string name;
float salary;
string department;
   // methods
void change_dept(string dept)
{
    department = dept;
}
void show_details()
{
   cout<<srn<<" "<<name<<" "<<salary<<" "<<department<<endl;
}
};

int main(){
    // creating a object
    Teacher t1;
    t1.srn = 890;
    t1.name = "neha";
    t1.salary = 90000;
    t1.department = "cse";
    t1.show_details();
    t1.change_dept("biotechnology");
    t1.show_details();
    return 0;
}
```
# SETTER AND GETTER FUNCTION FOR PRIVATE ATTRIBUTES OF A CLASS
Setter and getter functions (also known as mutator and accessor functions) are methods used to control access to the private attributes of a class. They are a fundamental part of encapsulation in object-oriented programming. Setters allow you to modify private variables, while getters allow you to retrieve their values.<BR/>
Why Use Setters and Getters?<BR/>
Encapsulation: Protect the internal state of the object.<BR/>
Validation: Perform checks or validation before modifying the value.<BR/>
Read-Only/Write-Only Access: Control how a class's attributes are accessed or modified.<BR/>
```
#include<iostream>
#include<string>
using namespace std;

class Teacher{
    private:   // access modifiers
    // attributes
int srn;
string name;
float salary;
string department;
   // methods
   public:

void setter(int new_srn,string newname,float newsalary,string newdepartment,int key)
{
    if(key == 2235){
        cout<<"access granted"<<endl;
        srn = new_srn;
        name = newname;
        salary = newsalary;
        department = newdepartment;
    }
    else{
        cout<<"access denied"<<endl;
    }

}
void getter()
{
   cout<<srn<<" "<<name<<" "<<salary<<" "<<department<<endl;
}
void change_dept(string dept)
{
    department = dept;
}
};

int main(){
    // creating a object
    Teacher t1;
    t1.setter(4567,"uday",78000,"bio",2235);
    t1.getter();
    t1.change_dept("civil");
    t1.getter();

    return 0;
}
```
we can access attributes inside a class easily, no matter, whether the attributes are private,public or protected. Generally we keep the attributes private and methods public to access these private attributes,and then ask for validation in these methods. Without public methods, since attributes are private, we cannot access from outside the class..
# ENCAPSULATION
Wrapping up attributes and methods in a single unit called class is encapsulation.<br/>
making a class id itself is an encapsulation.<br/>
it helps in data hiding of sensitive information by using private and protected access modifiers.<br/>
we cant access these sensitive info with . operator<br/>
![image](https://github.com/user-attachments/assets/82ead325-ffbb-45c6-874e-047708b37be9)
If you want to access them u have to define public methods inside that class.
# CONSTRUCTOR
![image](https://github.com/user-attachments/assets/039b70bf-3fba-42e1-9364-b36df2ab7af4)
## PARAMETERIZED CONSTRUCTOR
![image](https://github.com/user-attachments/assets/1cdd1662-92aa-4633-94f8-8b6c6e061303)
A parameterized constructor is a constructor that takes one or more arguments to initialize an object with specific values when it is created.
## DEFAULT CONSTRUCTOR
### Compiler provided
![image](https://github.com/user-attachments/assets/8e8fb701-20e6-48bb-98f9-ad0893325864)
Attributes wil be empty 
### User defined
![image](https://github.com/user-attachments/assets/01b8c126-b082-4f58-9f99-2d93f7fec0a8)
## COPY CONSTRUCTOR
![image](https://github.com/user-attachments/assets/5ede2ef6-21e2-4d5a-8ceb-8891d8725973)
Used when you want to make a new object by deep copying a existing object.
You make a object by using default, parameterised constructor and then make a neww object by deep copying the existing one.
# CONSTRUCTOR OVERLOADING IN C++ : POLYMORPHISM
Overloading in Constructors are the constructors with the same name and different parameters (or arguments). Hence, the constructor call depends upon data types and the number of arguments.
![image](https://github.com/user-attachments/assets/a0953188-c84c-4f09-a260-f5544661d4ec)







