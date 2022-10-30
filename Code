#include <iostream>
#include <cmath>
#include <algorithm>
#define ll long long
 
using namespace std;

int gcd(int a, int b) {
    if(a == 0) {
        return b;
    }
    int a1 = b % a;
    int b1 = a;
    int x = gcd(a1, b1);
    return x;
}

int lcm(int a, int b) {
    int g_c_d;
    if(a < b) g_c_d = gcd(a, b);
    else    g_c_d = gcd(b, a);

    return a*b/g_c_d;
}

int main() {
    int k, l, m, n;
    int d;
    cin >> k >> l >> m >> n;
    cin >> d;
    int N1 = d / k + d / l + d / m + d / n;
    int N2 = d / lcm(k,l) + d / lcm(k,m) + d / lcm(k,n) + d / lcm(m,l) + d / lcm(n,l) + d / lcm(m,n);
    int N3 = d / lcm(lcm(k,l),m) + d / lcm(lcm(k,l),n) + d / lcm(lcm(k,m),n) + d / lcm(lcm(n,l),m);
    int N4 = d / lcm(lcm(lcm(k,l),m),n);
    cout << N1 - N2 + N3 - N4;
    return 0;
}
