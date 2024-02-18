Welcome to the MyCpp wiki!
# 1. Constructor 
When an object of the class is defined, the compiler will invoke the default constructor implicitly to construct its object of the class type.
There are two types of constructors in C++: **default constructor** and **custom constructor**.

**Default constructor**: It is the special member function of the class, it has no return type and no parameter. Normally, it is implemented to construct an object of the class such as initializing the initial state of member variables, printing out some texts,...

Example of declaration of a default constructor:
> ###### class Cube {
> > ###### public:
> > > ###### Cube(): length_(0) {}; // default constructor
> > ###### private:
> > > ###### float length_;
> ###### };

**Custom constructor**: Like the default constructor, it is a special member function with no return type, but it has one or more parameters.
The custom constructor is also called a parameter constructor.

Example of a custom constructor:
> ###### class Cube {
> > ###### public:
> > > ###### Cube(): length_(0) {}; // default constructor
> > > ###### Cube(float l) : length_(l) {}; // custom constructor or parameterize constructor
> > ###### private:
> > > ###### float length_;
> ###### };
# 2. Copy constructor
A copy constructor is a special member function that exists to make a copy of an existing object.
![Screenshot from 2024-01-14 17-39-41](https://github.com/sonhongly/MyC-/assets/74746181/63092404-4eda-43fa-9788-60663c69f61a)
## 2.1 Automatic copy constructor
If no custom copy constructor is provided, the compiler will provide the automatic copy constructor for the object which copies attributes from another existing object.
## 2.2 Custom copy constructor
A custom copy constructor is a special member function with exactly one parameter of the same type as the class. Notice that, the parameter must be a **const** **reference**.

Example of a custom copy constructor:
> Cube::Cube(**const** Cube **&** obj);
## 2.3 Copy constructor invocation
Often, the copy constructor is invoked automatically by:
- Passing an object as the argument
- Initializing a new object
- Returning an object from a function
