#  **Constant Usage**

## **1- Constant Variables in C++**
If you make any variable as constant, using const keyword, you cannot change its value. Also, the constant variables must be initialized while they are declared. <br />

*Example:* <br />

```ruby
int main
{
    const int i=10;
    const int j=i+10;  // works fine
    i++;    // this leads to compile time error
}
```


## **2- Constant Pointer**
Here, w is a pointer, which is const, that points to an int. Now we can't change the pointer, which means it will always point to the variable x but can change the value that it points to, by changing the value of x. <br />

*Example:* <br />

```ruby
int main
{
    int x=1;
    int* const w= &x;
}
```


## **3- Constant Function Argument**
We can make the return type or arguments of a function as const. Then we cannot change any of them. <br />

*Example:* <br />

```ruby
void f(const int i)
{
    i++; //error
}

const int g()
{
    return 1;
}
```


## **4- Defining Class Data members as Constant**
These are data variables in class which are defined using const keyword. They are not initialized during declaration. Their initialization is done in the constructor and can't be changed again. <br /

*Example:* <br />

```ruby
class Test
{
    const int i;
    public:
    Test(int x):i(x)
    {
        cout << "\ni value set: " << i;
    }
};
int main()
{
    Test t(10);
    Test s(20);
}
```



# **Ampersand Usage**

## **1- Bitwise Operation**
Used as a Bitwise and logical operator. <br />

The & (bitwise AND) in C or C++ takes two numbers as operands and does AND on every bit of two numbers. <br />

*Example:* <br />

```ruby
int main()
{

    int a=5, b=9;
    //a=5(00000101), b=9(00001001)

    cout<< "a = "<< a <<","<<" b = "<< b << endl;
    cout<< "a & b = "<<( a & b) << endl;
    // the result is 00000001
}
```



## **2- Declare a reference to a type**
If you use & in the left-hand side of a variable declaration, it means that you expect to have a reference to the declared type. It can be used in any type of declarations (local variables, class members, method parameters).<br />

```ruby
int main()
{

   std::string x("Moe");
   std::string& y=x;
}
```

This doesn't just mean that both x and y will have the same value, but they will actually point to the same place in the memory.
