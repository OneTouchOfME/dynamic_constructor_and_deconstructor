# dynamic_constructor_and_deconstructor

#include <iostream>
using namespace std;
class A{
  int *x;
  public:
  A(){ 
      x=new int();
      cout<<"no parameter"<<endl;
   }
  void set_value(int y){*x=y;}
    A(int y)
     {    x=new int;
          *x=y;
          cout<<"one parameter"<<endl;
     }
   ~A(){
      delete x;
      cout<<"deleted"<<endl;
    }
};


int main(){
   
    
    A*obj = new A();
    obj->set_value(10);
    delete obj;
    
}
