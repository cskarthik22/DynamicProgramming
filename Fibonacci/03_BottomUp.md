```cpp

#include <bits/stdc++.h>

using namespace std;

int fib(int n) {
  if( n==0 || n==1 ) return 1;
  
  int a = 1, b = 1, c;

  for (int i=2; i<=n; i++) {
      c = a + b;
      a = b;
      b = c;
  }
  return c;
}

int main() {
  
  int n;
  
  cin >> n;
  cout << fib(n) << endl;
  
}

```
