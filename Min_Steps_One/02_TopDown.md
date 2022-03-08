

```cpp

#include <bits/stdc++.h>
using namespace std;

int min_steps_one(int n, int dp[]){
    if(n==1) return 0;
    
    if(dp[n] !=0) return dp[n];
    
    int op1,op2,op3;
    op1 = op2 =op3 = INT_MAX;
    
    if(n%3 == 0) op1 = 1 + min_steps_one(n/3, dp);
    if(n%2 == 0) op2 = 1 + min_steps_one(n/2, dp);
    op3 = 1 + min_steps_one(n-1, dp);
    dp[n] = min(min(op1,op2),op3);
    
    return dp[n];
}

int main() {
    int n;
    cin >> n;
    int *dp = new int[n+1];
    for(int i=0; i<=n; i++) {
        dp[i] = 0;
    }
    cout << min_steps_one(n, dp);
}

```
