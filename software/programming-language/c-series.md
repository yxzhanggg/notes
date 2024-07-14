---
layout: default
---
---
title: /C
layout: page
permalink: /C/
---
# Specifier
```c
// Lifetime all belows are the whole program runtime

// Global among files
// -file 1
int x;
// -file 2 can access x by declaring extern
extern int x; // Declare outside any function (usually in header file)
              // Defualt value 0
x = 1;

// Private to the file
static int x; // defualt value 0

// Store it in register
register int x;

// make the variable volatile to external change by forcing it to fetch its value(state) from main memory on every IO
// [The true state of a program/variable is always storing on virtual memory system (main memory)]
volatile int x;
```
# Array
```c
// The size of array is determined at compile time.
// Compared with fixed-size array, pointer array is more compatible 
// with heterogeneous data structure
char arr[3][2]; // Fixed-size array

char *arr[3];   // Pointer array: an array of 3 pointers to chars
char **arr;     // Pointer to pointer to char
char (*p)[3];   // A pinter to an array of 3 chars

//                 +---+         +---+---+---+---+---+
// argv ---------->| 0 |-------->| p | r | o | g | 0 |
//                 +---+         +---+---+---+---+---+
//                 | 1 |-------->| - | a | b | 0 |
//                 +---+         +---+---+---+---+
//                 | 2 |-------->| - | c | 0 |
//                 +---+         +---+---+---+---+---+---+
//                 | 3 |-------->| H | e | l | l | o | 0 |
//                 +---+         +---+---+---+---+---+---+
//                 | 4 |-------->| W | o | r | l | d | 0 |
//                 +---+         +---+---+---+---+---+---+
//                 | 5 |-------->NULL
//                 +---+
*++argv[0];      // equals *++(argv[0]), increase the pointer argv[0],
                 // then dereference (*), which equals 'r' in the case
(*++argv)[0];    // increase the pointer argv, then dereference by *,
                 // then dereference by [0] to the first element,
                 // which equals '-' in the case
                 
#include <string.h>
size_t strlen(const char *str);
char *strcpy(char *destination, const char *source);
char *strcat(char *destination, const char *source);
int strcmp(const char *str1, const char *str2);
char *strchr(char *str, int character);
```
# function
```c
int foo();          // a simple function declaration
int *foop();        // a function returns a pointer to int
foo;                // the adress of the function, anology of array
int (*pfoo)();      // foo is a pointer to the function
char (*(*x())[])(); // function returning pointer to array of pointer
                    // to function returning char
char (*(*x[])())[]; // array of pointer to function returning pointer
                    // to array of char
```
# sturcture
```c
struct point {
  int x;
  int y;
 };
sturct point *pp; // Pass large structure using pointer
// structure operator . ->
(*pp).x;
pp->x;

// Binary tree
struct tnode {         // The tree node
  char *word;          // Points to the text
  int count;           // Number of occurrences
  struct tnode *left;  // Left child
  struct tnode *right; // Right child
};

union {
  int ival;
  float fval;
  char *sval;
} u;

struct { // bit-field: only take 1-bit without address
  unsigned int is_keyword : 1;
  unsigned int is_extern : 1;
  unsigned int is_static : 1;
} flags;
```
# Lookup idom
```c
for (ptr = head; ptr != NULL; ptr = ptr->next)
```

# File I/O
stdin, stdout, stderr: 3 constant pointers to 3 FILE stucture.
```c
#include <stdio.h>

int getchar(void);            // Returns the next input(stdin) character or EOF
int putchar(int);             // Puts the 'int' on the stdout(defualt), returns the character written or EOF
int printf(char *format, arg1, arg2, ...); // Returns the number of characters printed or EOF
int scanf(char *format, ...); // Returns the number of characters printed or EOF
                              // Reads characters from the standard input, arguments must be pointers (&x)
int sprintf(char *string, char *format, arg1, arg2, ...); // Same above but to string
int sscanf(char *string, char *format, arg1, arg2, ...);
int fprintf(FILE *fp, char *format, ...); // Same above but to file
int fscanf(FILE *fp, char *format, ...);

// Every file in Linux has FILE structure which is defined by typedef
FILE *fp;
FILE *fopen(char *name, char *mode); // mode == ("r" || "w" || "a"); binary file: mode == ("rb" || "wb" || "ab");
fp = fopen(char *name, char *mode);  // Returns a pointer to a FILE structure
int fclose(FILE *fp);                // Break the pointer connection, return 0 or EOF
int getc(FILE *fp);                  // Returns the next character from the stream referred to by fp or EOF
                                     // Advance the position indicator for the stream
int putc(int c, FILE *fp);           // Writes the character c to the file fp and returns the character written
                                     // Advance the position indicator for the stream
// Relations between get/put|c/char
#undef getchar
#undef putchar
#define getchar() getc(stdin)
#define putchar(c) putc((c), stdout)

exit(0); // Equivalent return 0; calls fclose for each open output file, to flush out any buffered output.
int ferror(FILE *fp); // File error: return non-zero of file fp when error
int feof(FILE *fp);   // analogy above

char *fgets(char *line, int maxline, FILE *fp) // Returns line or NULL
int fputs(char *line, FILE *fp); // Return non-negative or EOF
gets; // Deletes the terminating '\n', Same above but from stdin
puts; // Adds the terminating '\n'
int ungetc(int c, FILE *fp); // Push char c to file fp, return c or EOF
```
# Miscellaneous functions
```c
// String Operations
#include <string.h>
strcat(s,t);    // Concatenate t to end of s
strncat(s,t,n); // Concatenate n characters of t to end of s
strcmp(s,t);    // Return negative, zero, or positive for s < t, s == t, s > t
strncmp(s,t,n); // Same as strcmp but only in first n characters
strcpy(s,t);    // Copy t to s
strncpy(s,t,n); // Copy at most n characters of t to s
strlen(s);      // Return length of s
strchr(s,c);    // Return pointer to first c in s, or NULL if not present
strrchr(s,c);   // Return pointer to last c in s, or NULL if not present

#include <ctype.h>
isalpha(c); // Non-zero if c is alphabetic, 0 if not
isupper(c); // Non-zero if c is upper case, 0 if not
islower(c); // Non-zero if c is lower case, 0 if not
isdigit(c); // Non-zero if c is digit, 0 if not
isalnum(c); // Non-zero if isalpha(c) or isdigit(c), 0 if not
isspace(c); // Non-zero if c is blank, tab, newline, return, formfeed, vertical tab
toupper(c); // Return c converted to upper case
tolower(c); // Return c converted to lower case

system(char *s); // Executes the command s, then resume, return whatever s returns

void *malloc(size_t n); // Returns a pointer to n bytes of uninitialized storage or NULL
void *calloc(size_t n, size_t size); // Same above but array[n] each object with the size
free(p); // Frees the space pointed to by p from malloc or calloc
// Free a list
for (p = head; p != NULL; p = q) {
  q = p->next;
  free(p);
}

#include <math.h> // They take double type, return double type
sin(x);   // sine of x, x in radians
cos(x);   // cosine of x, x in radians
atan2(y,x); // Arctangent of y/x, in radians
exp(x);   // Exponential function ex
log(x);   // Natural (base e) logarithm of x (x>0)
log10(x); // Common (base 10) logarithm of x (x>0)
pow(x,y); // x^y
sqrt(x);  // Square root of x (x>0)
fabs(x);  // Absolute value of x

#include <stdlib.h>
rand();          // Computes a sequence of pseudo-random integers in the range zero to RAND_MAX
srand(unsigned); // Sets the seed of rand
// Produce random floating-point numbers greater than or equal to zero but less than one
#define frand() ((double) rand() / (RAND_MAX+1.0))
```
# Acknowledgement
Thanks Brian Kernighan and Dennis Ritchie for the "The C Programming Language"! The book is at an introductory level but some basic knowledge about discrete math, Unix, and computer system are required, but it indeed provides concise information for learning C language.

As Unix is written in C, it is also good introductory material to get in touch with the Unix kernel.


# C++
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
