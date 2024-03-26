# finding the lowest positive missingelement
This c++ code helps you find the lowest missing positive elements in an array/Vector
#include<iostream>
#include<vector>
#include<algorithm>
using namespace std;
int findTheLowestMissingElement(vector<int> a){
    std::sort(a.begin(),a.end());
    int n=1;
    for(int i=0;i<a.size();i++){
        if(a[i]<=0||(i>0&&a[i]==a[i-1])){
            continue;
        }
    if(a[i]!=n)
    return n;
    n++;
    }
return n;
}
int main(){
    vector<int> a;
    int n;
    cout<<"Enter the size of the vector:";
    cin>>n;
    cout<<"Enter the elements of the vector";
    for(int i=0;i<n;i++){
       int input;
       cin>>input;
        a.push_back(input);
    }
    cout<<"The missing element in the vector is : "<<findTheLowestMissingElement(a);
    /* for example 
    constraints: The time complexity should be O(n)
    0,1,-1,9,8
    it has a range from 1 to 9 but the lowest missing element is 
    -1,0,1,8,9
    there are some missing elements but the lowest missing positive element is 2
    */
}
