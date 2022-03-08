

```cpp

#include <iostream>
#include <bits/stdc++.h>
using namespace std;

int min_steps_one(int n){

    if(n==1) return 0;
    
    int op1,op2,op3;
    op1 = op2 =op3 = INT_MAX;
    
    if(n%3 == 0) op1 = 1 + min_steps_one(n/3);
    if(n%2 == 0) op2 = 1 + min_steps_one(n/2);
    op3 = 1 + min_steps_one(n-1, dp);
    
    return min(min(op1,op2),op3);
}
int main() {
    int n;
    cin >> n;
    cout << min_steps_one(n);
}

```
