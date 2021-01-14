# 1---sum-of-inverse-even-factorials-with-same-number-on-top

#include <iostream>
using namespace std;


int main(){
    int n;
    cout << "Enter the value of N: ";
    cin >> n;
    cout << 1 << " -";
    for(int i=2; i<=n; i+=2){
        cout << " ("<< i << "/" << i << "!) + ";
    }

    cout << "\b\b= ";

    float sum = 0;

    for(float i=2; i<=n; i+=2){
        float s = 1;
        for(int j=1; j<=i; j++){
                s = j*s;
        }
        sum = sum + (i/s);
    }
    cout << 1-sum;
    return 0;
}
