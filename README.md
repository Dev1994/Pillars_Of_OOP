# Pillars_Of_OOP
The four pillars for OOP are Abstraction, Encapsulation, Inheritance, Polymorphism. Abstraction : Abstraction is the process of showing only essential/necessary features of an entity/object to the outside world and hide the other irrelevant information.

# Object Oriented Programming
A programming model which is mainly organized around the objects is called Object Oriented Programming or the Programming where the main focus of programmer while modeling any problem is objects. (The name OOP indicates the same).

# What is Class?
Class is a template/blueprint for the Objects. It defines the object behavior (in the form of class methods) and object attributes (in the form of properties or class data members).

## 1. What Is Encapsulation
Encapsulation is a process of binding data members (variables, properties) and member functions (methods) together. In object oriented programming language we achieve encapsulation through Class.

### Real Life Example Of Encapsulation:
The real life example of encapsulation will be the Capsule. Capsule binds all chemical contents required for curing specific disease together just like the class which binds data members and member functions.

```c#
Public Class Account  
{  
       private double balance;  
       public double GetBalance()  
       {  
         return balance;  
       }  
}  
//Imagine main as outside world  
public static void Main()  
{  
        Account obj=new Account();  
        double currentBalance=obj.GetBalance();  
   
        //Following thing is not possible  since that data member is private   
        obj.balance=20000000000;  
}
```

## 2. What Is Abstraction
Abstraction is the process of showing only essential/necessary features of an entity/object to the outside world and hide the other irrelevant information.
In programming language we achieve the abstraction through public and private access modifiers and a class. So in a class make things (feature) which we want to show as public and thing which are irrelevant make them as private so they won't be available to the outside world.

### Benefits/Advantages Of Using Abstraction:
Advantage of Abstraction is, it reduces the complexity of end users since to the end user we have shown only things that are necessary to him and not shown the unnecessary things.

## 3. What Is Inheritance
The process of creating the new class by extending the the existing class is called inheritance or the process of inheriting the features of base class is called as inheritance.
The existing class is called the base class and new class which is created from it is called the derived class.

### Real Life Example Of Inheritance:
We inherit some of our features (may be body color, nose shape, height of body etc) from Mom and Dad.

### Benefits/Advantages Of Using Inheritance:
The most important advantage of inheritance is code re-usability. In Inheritance the derived class possess all attributes/properties and functions of base class, this is where code re-usability comes into the picture. So no need to write same function and attributes of base class in derived class.

#### Implementation Of Inheritance In Programming Language:

```c#
//suppose initially I wrote a base class shape as   
class Shape  
{  
     public int width;  
     public int height;  
     public void SetWidth(int w)  
     {  
        width=w;  
     }  
     public void SetHeight(int h)  
     {  
        height=h;  
     }  
}  
  
  
//derived class rectangle  
class Rectangle:Shape  
{  
       public int GetArea()  
       {  
         return width * height;  
       } 
{
```
```c#
      static void Main()  
      {  
          //Derived class object  
          Rectangle obj=new Rectangle();  
          obj.SetWidth(5);  
          obj.SetHeight(10);  
          Console.WriteLine(“Area of rectangle is {}”,obj.GetArea());  
          Console.Read()  
      }  
}  
```
## 3. What Is Polymorphism
Poly means many and Morph means forms. Polymorphism is the process in which an object or function take different forms.
Real Life Example Of Polymorphism:
Real life example of Polymorphism is mobile phone. It is a single object but it can be used for making calls, listening music, sending mails, taking pictures, etc (different forms).

```c#
//Implementation of polymorphism using method overloading  
class Base  
{  
      public int Add(int num1,int num2)  
      {  
              return(num1+num2);  
       }  
      public int Add(double num1,double num2)  
      {  
              return(num1+num2);  
      }   
}  
class Program  
{  
      public static void Main()  
      {  
            Base obj=new Base();  
            Console.WriteLine(“Addition of two integer number is ”+obj.Add(4,5));  
            Console.WriteLine(“Addition of two float number is ”+obj.Add(6.78,5.23));  
    
       }  
}  
```

### Advantages/Benefits Of Using Polymorphism:
The main advantage of polymorphism is, it makes the life of end user easy since instead of having two methods (as shown in above example) AddInt for adding integer and AddFloat for adding the float we have only one method Add. So end user have to remember only Add method and not AddInt and AddFloat.
