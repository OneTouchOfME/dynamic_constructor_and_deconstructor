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




//dynamic array of three elelment

#include <iostream>
using namespace std;
class A{
  int *arr;
  public:
  A(){ 
      arr=new int[3];
      cout<<"no parameter"<<endl;
  }
  void set_value(int *a,int sz){
      for(int i=0;i<sz;i++){
          arr[i]=a[i];
      }
  }
  void display(int sz){
      for(int i=0;i<sz;i++)cout<<arr[i]<<" ";
      cout<<endl;
  }
//   A(int y)
//   {    x=new int;
//       *x=y;
//       cout<<"one parameter"<<endl;
//   }
   ~A(){
      delete []arr;
      cout<<"deleted"<<endl;
    }
};


int main(){
   int a[3]={1,2,3};
   A*obj=new A();
   obj->set_value(a,3);
   obj->display(3);
   //delete obj;   
   
 
}
