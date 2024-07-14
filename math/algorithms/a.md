---
layout: default
title: algorithm
---
# Loop invariant
1. Initialization: It is true prior to the ﬁrst iteration of the loop.
2. Maintenance: If it is true before an iteration of the loop, it remains true before the next iteration.
3. Termination: When the loop terminates, the invariant gives us a useful property that helps show that the algorithm is correct.

# Recurrence
Reccurence is one type of loops (loop itself).
Rules:
1. Base cases. You must always have some base cases, which can be solved without recursion.
2. Making progress. For the cases that are to be solved recursively, the recursive call must always be to a case that makes progress toward a base case.
3. Design rule. Assume that all the recursive calls work.
4. Compound interest rule. Never duplicate work by solving the same instance of a problem in separate recursive calls.

```c++
void getInput(){
    char c; // initialization
    if( std::cin.get(c) && c!='\n' ){ // '\n' is the false of maintenance
        getinput()
    }
    std::cout.put(c) // the termination that outputs the useful thing
}

int fibonacciSequence(int x) { // the input x is the initialization
   if( (x==1)||(x==0) ) { // x=1 or x=0 is the false of maintenance
      return(x); // the termination that outputs the useful thing
   }
   else {
      return( fib(x-1)+fib(x-2) ); // maintainance, every loop it chances the input x by expression x-1 and x-2
   }
}
```
# Sort
Sort = comparison + exchange + loop invariant
```c++
void swap(void *v[], int i, int j)
{
  void *temp,
  temp = v[i];
  v[i] = v[j];
  v[j] = temp;
}
```
# Quick power
```c++
// decimal to binary: 10 = 1 0 1 0 
//                         8 4 2 1
//                    a^10 = a^8 * a^2

int quick_pow(int a, int b) {
  int temp = a, ans = 1;
  while (b) {
    if (b % 2) {
    ans = ans * temp;
    }
  b /= 2;
  temp = temp * temp;
  }
  return ans;
}

int main() {
  int a, b;
  while (cin >> a >> b) {
  cout << quick_pow(a, b) << endl;  
  return 0;
  }
}
```
