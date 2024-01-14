Welcome to the MyC- wiki!
# 1. Constructor 
>
When an object of the class is defined, the compiler will invoke the default constructor implicitly to construct its object of the class type.
There are two types of constructors in C++: **default constructor** and **custom constructor**.
>
**Default constructor**: It is the special member function of the class, it has no return type and no parameter. Normally, it is implemented to construct an object of the class such as initializing the initial state of member variables, printing out some texts,...
> 
Example of declaration of a default constructor:

> ###### class Cube {
> > ###### public:
> > > ###### Cube(): length_(0) {};
> > ###### private:
> > > ###### float length_;
> ###### };
>
**Custom constructor**: Like the default constructor, it is a special member function with no return type, but it has one or more parameters.
The custom constructor is also called a parameter constructor.
>
Example of a custom constructor:
> ###### class Cube {
> > ###### public:
> > > ###### Cube(): length_(0) {};
> > > ###### Cube(float l) : length_(l) {};
> > ###### private:
> > > ###### float length_;
> ###### };
