---
title: /C++
layout: page
permalink: /C++/
---
# Iterator
```c++
std::string s{"12132s"};
itb = s.begin();
ite = s.end();
first_value = *itb;
```
# Lambda expression / Closure
A function without name
```c++
int N = 100, M = 300;
auto f = [N, &M](int i, int j] -> int { // Capture Clause: [&], [=], [&,=N], [this], [*this], [K=3] 
  M = 20;
  N = 20; // compiler error
  return i + j;
};
cout << f(1,2) << endl; // 3
cout << M << endl; // 20
```
# Classes
Initializer runs faster than assignment in class body.

# Reference
Reference is a synomym of the original value, but not an object (pointer is an object).
```c++
// lvalue (stable value) reference
// 1. aliasing
int asddsdsdasdasd = 1;
int &b = asddsdsdasdasd;
b = 3;
// 2. avoiding copy large things
auto &x = findMax(arr); // Returns large value
// call-by-reference-to-a-constant / call-by-constant reference (equivalent to call-by-value but smaller memory)
string randomItem(const vector<string> &arr); // call in large array but without requirememt of copying
// 3. passing parameters - call-by-lvalue-reference
void swap( double & a, double & b );
// range loop to change value
for (auto &x : arr) { // without '&', x is a copy of the original one
  ++x;
}

// rvalue (temporary value) reference
string &&c = "hello";
string randomItem(vector<string> &&arr); // overloading randomItem
vector<string> v {"hello", "world"};
cout << randomItem(v) << endl; // invokes lvalue method
cout << randomItem({"hello", "world"}) << endl; // invokes rvalue method
// cast any value into rvalue, avoid copying
y = std::move(x);

// return type
const LargeType &item3 = randomItem2(vec); // Return-by-constant-reference:
                                           // return a non-modiﬁable value such as a value in an array
vector<int> sums = partialSum(vec); // Copy(memory allocation) in old C++; move(changing pointer) in C++11
```
# Constructors
lvalue invokes copy constructor/assignment, rvalue invokes move constructor/assignment.
```c++
explicit IntCell(int i) : i_(i); // Avoid implicit conversion (potential error)
~IntCell(); // Deconstructor
IntCell(const IntCell &rhs); // Copy constructor
IntCell(IntCell &&rhs); // Move constructor 
IntCell &operator=(const IntCell &rhs); // Copy assignment
IntCell &operator=(IntCell &&rhs); // Move assignment

```
# [C++11]Smart pointer
```c++
unique_ptr<someType> suniquePtr(new someType(args));
...
uniquePtr.release();
shared_ptr<someType> somePtr(new someType(args));
weak_ptr<someType> weakPtr= somePtr;
```
# Virtual function
```c++
class A {
  public:
   virtual const char* fetchClassName() { return "A"; }
};

class B: public A {
  public:
   const char* fetchClassName() { return "B"; }
};

class C: public B {
  public:
   const char* fetchClassName() { return "C"; }
};

int main(void) {
  C obj_c;
  A &obj_a = obj_c;   
  std::cout << obj_a.fetchClassName() << "\n"; // Output: C
  B obj_b;
  A &obj_a = obj_b;   
  std::cout << obj_a.fetchClassName() << "\n"; // Output: B
}
```
# Friend
```c++
// Bridging and accessing
// A friend class can access private and protected members of other class in which it is declared as friend.
// All access granted.
class A {  
  friend class B; // [not member] Just declaration, does not belong to any member of public, protected or private
                  // members in B can access members of A
  friend int B::bar(); // only member function bar() of B can access members of A
  friend int foo(A, B); // Friend function just as Friend Class
  private:
   int x_;
};

class B {
  friend void foo(A, B);
  public:
   int bar();
  private:
   int x_;
};

int foo(A a, B b) {
  return a.x_+b.x_;
}
```
# Conventions
Use`{}` for initialization, use `=` for copying, use `()` for arguments transfer.
