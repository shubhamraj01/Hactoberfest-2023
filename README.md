# Hactoberfest-2022
/*Program for
accessing Private data using protected class in C++*/

#include <iostream>
using namespace std;
 class base{
     protected:
     int x;
     public:
     void setdata(int var1){
        x=var1;
     } };
 class derived:protected base{
     
     int x=13;
     public:
     void display(){
        cout<<x<<endl;
     }
     friend void value(derived a);
 };
 void value(derived a){
cout<<a.x;
}
 int main(){
     derived d;
     d.display();
 } 
