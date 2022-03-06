
```cpp

#include <bits/stdc++.h>

using namespace std;

int fib(int n, int* cache) {
  if( n==0 || n==1 ) cache[n] = 1;
  
  if(cache[n] != 0) return cache[n];
  
  cache[n] = fib(n-1, cache) + fib(n-2, cache);
  return cache[n];
  
}

int main() {
  int n;
  cin >> n;
  int *cache = new int[n+1];
  for(int i=0; i<=n; i++) {
    cache[i] = 0;
  }
  cout << fib(n, cache) << endl;
  
}
```
