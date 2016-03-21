#Advanced Game Programming – Assignment 1: Obtaining 400 points on Hackerrank

Hackerrank nickname: eliodeb

Hackerrank profile link:  http://www.hackerrank.com/eliodeb

Domains, points and current rank:
-	 **C/C++**

 Points: **571**

 Rank:   **161**

-	**Algorithm (solved in C++)**

 Points: **256**

 Rank:   **61743**

**Total Points: 827**

##Introduction

The aim of this coursework was to obtain at least 400 points on the website “Hackerrank” that provides users with many problems in different areas of programming and using different languages such as C/C++, Java, Python etc.
I am currently learning C++ so I solved all my exercises using this programming language. Specifically the domains that I worked on Hackerrank were “C/C++” that contains exercises specifically designed for this language and “Algorithm” where the exercises can be solved in your preferred language. Once again, I used C++ in all the tasks I solved there as well.

###C/C++ Domain

In this domain the different tasks are grouped in 5 main areas: Introduction, Strings, Classes, STL and Inheritance. 

In introduction all the basic data types, loops, functions, containers, pointers, conditional statements, the concept of operator overloading and virtual functions are introduced with different and increasingly challenging exercises.

In the string subset the tasks aim at teaching the use of the type string and the operation that are allowed with it.

The classes subset sets the foundation for object oriented programming starting with simple exercises on class definition all the way to abstraction and polymorphism.

The STL subset presents tasks to get familiar with common STL containers, classes, functions and Algorithms.

Finally in inheritance the concept of linking multiple classes is presented and developed through a few clever tasks. 

I found this Domain very useful and I finally made some order in my C++ knowledge while adding new concepts, techniques and tricks. I completed almost all the tasks in this domain except for a few very hard ones that I will work on in the future. All the tasks I solved in this domain are listed at the end of this report with my code solution. For brevity reasons I only wrote the name of the challenge and the domain it belongs to as the exercises instructions can be easily found on the Hackerrank website with the information provided in this report.


###Algorithm Domain

In the algorithm domain users can solve the challenges is their preferred language. As previously mentioned I solved all the exercises in C++. In this domain there are also several subdomain starting from easy and general warmup challenges all the way up to game theory and bit manipulation. I concentrated on the “Warmup” and “Implementation” subsets.

In Warmup the challenges revolve mostly around simple math tasks, matrices manipulation and time conversion.

In Implementation the tasks become more varied and complicated requiring extra use of logic skills among more refined optimization techniques and a deeper understanding of math and number theory.

In this domain I could test my logic skills as well as applying what I learned in the C++ section. I found that the community on the website was very helpful and you get quick replies with hints that lead you to the solution stimulating your thinking. I was glad I could contribute in giving advice to other users when I could figure out a good solution to some of the problems.
I will definitely continue solving challenges in this domain to further improve my C++ programming skills. I also plan on using this website to practice coding in Python in the future.
Once again, the challenges I solved are listed below and separated in their subdomains. The challenge names are clearly listed with my code solution right after. Full challenge details can be found on Hackerrank as previously stated.

#Challenges Solved with solution code

Below are listed all the challenges I solved sorted by their main domain and subdomain.

##C/C++ Domain

###Introduction:

 - **Hello, World !**
```cpp
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    printf("Hello, World!");
    return 0;
}
```

 - **Input and Output**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    int a,b,c,sum;
    
    cin>>a>>b>>c;
    sum = a+b+c;
    cout<<sum;
    return 0;
}

```
 - **Basic Data Types**
```cpp
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    int a;
    long b;
    long long c;
    char d;
    float e;
    double f;
    
    scanf("%d %ld %lld %c %f %lf", &a, &b, &c, &d, &e, &f);
    
    printf("%d\n%ld\n%lld\n%c\n%f\n%lf", a , b,c,d,e,f);
    
        
    return 0;
}
```

 - **Conditional Statements**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
 unsigned int n;
    cin>>n;
    
    if(n>=1 && n<=9)
        {
        
        if      (n==1){cout<<"one";}
        else if (n==2){cout<<"two";}
        else if (n==3){cout<<"three";}
        else if (n==4){cout<<"four";}
        else if (n==5){cout<<"five";}
        else if (n==6){cout<<"six";}
        else if (n==7){cout<<"seven";}
        else if (n==8){cout<<"eight";}
        else if (n==9){cout<<"nine";}
    }
    
    else {cout<<"Greater than 9";}
 
   return 0;
}
```

 - **For Loop**
```cpp
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    int a,b;
    
    cin>>a;
    cin>>b;
    
    for(int i=a;i<=b;i++)
        {
        if(i<=9)
            {
            if     (i==1){cout<<"one"<<endl;}
            else if(i==2){cout<<"two"<<endl;}
            else if(i==3){cout<<"three"<<endl;}
            else if(i==4){cout<<"four"<<endl;}
            else if(i==5){cout<<"five"<<endl;}
            else if(i==6){cout<<"six"<<endl;}
            else if(i==7){cout<<"seven"<<endl;}
            else if(i==8){cout<<"eight"<<endl;}
            else if(i==9){cout<<"nine"<<endl;}
        }
        
        else{
            
            if(i%2==0){cout<<"even"<<endl;}
            else      {cout<<"odd"<<endl;}
            
        }
        
    }
    return 0;
}
```

 - **Functions**
```cpp
#include <iostream>
#include <cstdio>
using namespace std;


int max_of_four(int a, int b, int c, int d){
    
    int max=a;
    if(b>max){max=b;}
    if(c>max){max=c;}
    if(d>max){max=d;}
    
    return max;
}


int main() {
    int a, b, c, d;
    scanf("%d %d %d %d", &a, &b, &c, &d);
    int ans = max_of_four(a, b, c, d);
    printf("%d", ans);
    
    return 0;
}
```


 - **Pointer**
```cpp
#include <stdio.h>

void update(int *a,int *b) {
    int tempA;
    int tempB;
    
    tempA=*a+*b;
    
    if(*a>*b) {tempB=*a-*b;}
    else      {tempB= *b-*a;}
    
    *a=tempA;
    *b=tempB;
}

int main() {
    int a, b;
    int *pa = &a, *pb = &b;
    
    scanf("%d %d", &a, &b);
    update(pa, pb);
    printf("%d\n%d", a, b);

    return 0;
}
```

 - **Arrays Introduction**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    int N;
    cin>>N;
    int arr[N];
    
    for(int i=0;i<N;i++)
        {
       
        cin>>arr[i]; 

       }
    
    for(int i=(N-1);i>=0;i--)
        {
        
        cout<<arr[i]<<" ";
    }
    
    
    return 0;
}
```

 - **Operator Overloading**
```cpp
class Matrix{
   
   public:
   vector<vector<int> > a; 
    
    Matrix & operator + (const Matrix &y){
        
           for (int m=0; m<y.a.size(); ++m) {
        for (int n=0; n<y.a[0].size(); ++n) {
            this->a[m][n] = this->a[m][n] + y.a[m][n];
        }
    }

    return *this;
    }
        
        
    
    
};
```

 - **Variable Sized Arrays**
```cpp
int n,q;

cin>>n>>q;

int** seq=new int* [n];
for(int i=0;i<n;i++)
    {
      int a;
      cin>>a;
      int* b=new int [a];
      for(int j=0;j<a;j++)
        {
          int e;
          cin>>e;
          b[j]=e;
        }
    *(seq+i)=b;
   }

  for(int i=0;i<q;i++)
  {
  int r,s;
  cin>>r>>s;
  cout<<seq[r][s]<<endl;
  }

	return 0;
}
```

 - **Overload Operators**
```cpp
//Overload operators + and << for the class complex
//+ should add two complex numbers as (a+ib) + (c+id) = (a+c) + i(b+d)
//<< should print a complex number in the format "a+ib"


Complex operator + (Complex k,Complex l ) 
{ Complex z; 
 z.a=k.a+l.a;
 z.b=k.b+l.b;
 return z;
} 

ostream& operator << (ostream& o,Complex z)
{
    return o << z.a << "+" << "i" << z.b << endl;
}
```

 - **Virtual Functions**
```cpp
static int professorID, studentID;
class Person
{
private:
string name;
int age;

public:
virtual void getdata() {
    cin >> name;
    cin >> age;
}
virtual void putdata() {
    cout << name << " " << age << " ";
}
};
class Professor : public Person
{
private:
int publication;
int id;

public:
Professor() {
    professorID++;
}
void getdata() {
    Person::getdata();
    cin >> publication;
    id = professorID;
}
void putdata() {
    Person::putdata();
    cout << publication << " " << id << endl;
}
};
class Student : public Person
{
private:
int marks[6];
int id;


public:
Student() {
    studentID++;
}
void getdata() {
    Person::getdata();
    for(int i = 0; i < 6; ++i)
        cin >> marks[i];
    id = studentID;
}
void putdata() {
    Person::putdata();
    int sum = 0;
    for(int i = 0; i < 6; ++i)
        sum += marks[i];
    cout << sum << " " << id << endl;
}
};
```

###Strings:

 - **Strings**
```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
   string a;
   string b;
   string a1;
   string b1;
    
    cin>>a;
    cin>>b;
    
    cout<<a.size()<<" "<<b.size()<<"\n";
    
    cout<<a+b<<"\n";
    
    a1=a;
    b1=b;
    
    a1[0]=b[0];
    b1[0]=a[0];
    
    cout<<a1<<" "<<b1;
  
    return 0;
}
```

 - **StringStream**

```cpp
#include <sstream>
#include <vector>
#include <iostream>
using namespace std;

vector<int> parseInts(string str) {
   stringstream ss(str);
   vector<int> final_vector;
   int temp;
   char ch;
    while(ss>>temp){
        
        final_vector.push_back(temp);
        ss>>ch;
        
    }
    
    return final_vector;
}

int main() {
    string str;
    cin >> str;
    vector<int> integers = parseInts(str);
    for(int i = 0; i < integers.size(); i++) {
        cout << integers[i] << "\n";
    }
    
    return 0;
}
```

###Classes:

 - **Structs**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

struct Student {
    
    int age;
    string first_name;
    string last_name;
    int standard;
    
};

int main() {
    Student st;
    
    cin >> st.age >> st.first_name >> st.last_name >> st.standard;
    cout << st.age << " " << st.first_name << " " << st.last_name << " " << st.standard;
    
    return 0;
}
```

 - **Class**
```cpp
#include <iostream>
#include <sstream>
using namespace std;

class Student{
     private:
    int age, standard;
    string first_name, last_name;
    stringstream ss;
    char ch = ',';
    
    public:
    
   void set_age(int age_){
        
        age = age_;
        
    }
    
    int get_age(){
        
        return age;
    }
    
   void set_first_name(string first_name_){
        
        first_name = first_name_;
        
    }
    
    string get_first_name(){
        
        return first_name;
    }
    
      void set_last_name(string last_name_){
        
        last_name = last_name_;
        
    }
    
    string get_last_name(){
        
        return last_name;
    }
    
     void set_standard(int standard_){
        
        standard = standard_;
        
    }
    
    int get_standard(){
        
        return standard;
    }
    
  string to_string()
  { 
 ss<<age<<ch<<first_name<<ch<<last_name<<ch<<standard;  
 return ss.str();
  }
    
    
    
};

int main() {
    int age, standard;
    string first_name, last_name;
    
    cin >> age >> first_name >> last_name >> standard;
    
    Student st;
    st.set_age(age);
    st.set_standard(standard);
    st.set_first_name(first_name);
    st.set_last_name(last_name);
    
    cout << st.get_age() << "\n";
    cout << st.get_last_name() << ", " << st.get_first_name() << "\n";
    cout << st.get_standard() << "\n";
    cout << "\n";
    cout << st.to_string();
    
    return 0;
}
```

 - **Classes and Objects**
```cpp
// Write your Student class here

class Student {
    
    private:
    int scores[5];
    
    
    public:
    
    void input(){
        
        int exam_score;
        
        for(int i=0;i<5;++i){
            
            cin>>exam_score;
            scores[i]=exam_score;
        }
        
    }
    
    int calculateTotalScore(){
        
        int total_score=0;
        
        for(int i=0;i<5;i++){
            
            total_score+=scores[i];
        }
        
        return total_score;
    }
    
    
};
```

 - **C++ Class Templates**
```cpp
/*Write the class AddElements here*/
template <class T> 
    
   class AddElements{ 
    public:
    
T element1,element2;
    
AddElements(T el){
    element1=el;
}
    
T add(T el2){
    return(element1+el2);
}
    
 T concatenate(T el2){
    return(element1+el2);
}
    
};
```

 - **Box It!**
```cpp
class Box {


private:
    
long l,b,h;
    
public:

Box(){
    
    l=0;
    b=0;
    h=0;
    
    BoxesCreated++;
}   
    
Box(int length, int breadth, int height){
    
    l=length;
    b=breadth;
    h=height;
    BoxesCreated++;
}

Box(Box& B){
    
    l=B.l;
    b=B.b;
    h=B.h;
    
    BoxesCreated++;
}
    
 ~Box()
{
     
BoxesDestroyed++;
     
 }


    
int getLength(){
    
    return l;
}
    
int getBreadth ()
    {
    
    return b;
}
    
    
 int getHeight (){
     
     return h;
 }
    
long long CalculateVolume(){
    
    
    return l*b*h;
}


bool operator<(Box &B){
    
    if ((l<B.l)||(b<B.b && l==B.l) || (h<B.h && b==B.b && l==B.l) )
    {return true;}
    

   
    else {return false;}
 
}

friend ostream& operator<<(ostream& out, Box B){
    
  out<<B.l<<" "<<B.b<<" "<<B.h;
  return out;
    
}

};
```

 - **Attending Workshops**
```cpp
//Define the structs Workshops and Available_Workshops.
//Implement the functions initialize and CalculateMaxWorkshops
struct Workshop {
    int start;
    int duration;
    int end;
};

struct Available_Workshops {
    int n;
    vector<Workshop> workshops;
};

struct sort_key
{
    inline bool operator() (const Workshop& struct1, const Workshop& struct2)
    {
        return (struct1.end < struct2.end);
    }
};

Available_Workshops* initialize(int start_times[], int durations[], int n) {
    Available_Workshops *ptr = new Available_Workshops();
    ptr->n = n;
    ptr->workshops = vector<Workshop>(n);
    for (unsigned i=0; i<n; ++i) {
        ptr->workshops[i].start = start_times[i];
        ptr->workshops[i].duration = durations[i];
        ptr->workshops[i].end = start_times[i] + durations[i];
    }
    
    return ptr;
}

int CalculateMaxWorkshops(Available_Workshops *ptr) {
    int count = 1;
    int current_end_index = 0;
    
    // OLD SORT, produces good result but gives timeout (it's slow)
    /*for (unsigned i=0; i<ptr->n-1; ++i) {
        for (unsigned j=i+1; j<ptr->n; ++j) {
            if (ptr->workshops[j].end < ptr->workshops[i].end) {
                Workshop temp = ptr->workshops[i];
                ptr->workshops[i] = ptr->workshops[j];
                ptr->workshops[j] = temp;
            }
        }
    }*/
    
    // NEW SORT
    std::sort(ptr->workshops.begin(), ptr->workshops.end(), sort_key());
    
    for (unsigned i=1; i<ptr->n; ++i) {
        if (ptr->workshops[i].start >= ptr->workshops[current_end_index].end) {
            ++count;
            current_end_index = i;
        }
    }
    
    return count;
}
```

###STL:

 - **Vector-Sort**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() 
{   
    int n;
    cin>>n;  
    int temp;
    
    vector<int> MyVector;
    
    for(int i=0;i<n;++i){
        
        cin>>temp;
        MyVector.push_back(temp);
        
    }
    
    std::sort(MyVector.begin(),MyVector.end());
    
    for(int i=0;i<n;++i){
        
        cout<<MyVector[i]<<" ";
        
        
    }
    
    
 
    return 0;
}
```

 - **Vector-Erase**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    
    int n;
    cin>>n;
    
    int x;
    int a,b;
    
    int temp;
    
    vector<int> MyVector;
    
    for(int i=0;i<n;++i){
        
        cin>>temp;
        MyVector.push_back(temp);
        
    }
    
    cin>>x;
    cin>>a;
    cin>>b;
    
    MyVector.erase(MyVector.begin() + x - 1);
    MyVector.erase(MyVector.begin() + a - 1 , MyVector.begin() + b - 1);
    
    cout<<MyVector.size()<<"\n";
    
    for(int i=0;i<MyVector.size();++i){
        
        cout<<MyVector[i]<<" ";
        
        
    }

    
    return 0;
}
```

 - **Lower Bound-STL**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    
    int n;
    cin>>n;
    
    int q;
    int y;
     
    int temp;
    
    vector<int> MyVector;
    vector<int> MyQuery;
    
    for(int i=0;i<n;++i){
        
        cin>>temp;
        MyVector.push_back(temp);
        
    }
    
    cin>>q;
    
    for(int i=0;i<q;++i){
        
        cin>>y;
        MyQuery.push_back(y);
        
    }
    
    std::vector<int>::iterator low;
    
    
    
      for(int i=0;i<q;++i){
        
          low = lower_bound(MyVector.begin(), MyVector.end(), MyQuery[i]);
          if    (MyVector[low - MyVector.begin()] == MyQuery[i]) {cout << "Yes " << (low - MyVector.begin()+1) << endl;}
          else                                                   { cout << "No " << (low - MyVector.begin()+1) << endl;}
          
           
    
        
    }
    
    
 
    return 0;
}
```

 - **Sets-STL**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <set>
#include <algorithm>
using namespace std;


int main() {
    
    set<int> s;
    int q;
    cin>>q;
    
    int x;
    int y;
    
    for(int i=0;i<q;++i){
        
        cin>>y;
        cin>>x;
        
        switch (y){
            case 1: s.insert(x);
                    break;
        
            case 2: s.erase(x);
                    break;
        
            case 3:
                   set<int>::iterator itr=s.find(x);
            
                   if   (itr != s.end()) {cout<<"Yes"<<endl;}
                   else                  {cout<<"No"<<endl;}
                   break;
        }
    }
    
    
    return 0;
}
```

 - **Maps-STL**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <set>
#include <map>
#include <algorithm>
#include <string>
using namespace std;


int main() {
    
    map<string,int> m;
    int q;
    cin>>q;
    int type;
    
    string name;
    int grade;
    
    map<string,int>::iterator itr;
    
    for(int i=0;i<q;++i){
        
        cin>>type;
        
        switch (type){
            
            
            case 1: cin>>name;
                    cin>>grade;
                    itr = m.find(name); 
                    if (itr == m.end()) {m.insert(make_pair(name, grade));}
                    else                {itr->second += grade;}
                    break;
        
            case 2: cin>>name;
                    m.erase(name);
                    break;
        
            case 3:cin>>name;
                   itr=m.find(name);
                   if(itr!=m.end()) {cout<<itr->second<<endl;}
                   else             {cout<<"0"<<endl;}
                 
                   break;
        }

        
        
    }
    
    
    return 0;
}
```
 - **Deque-STL**
```cpp
#include <iostream>
#include <deque> 
#include <vector>
using namespace std;

void printKMax(int arr[], int n, int k)
{
    int max = arr[0];
    int imax = 0;
    for (int i=1; i<k; ++i)
    {
        if (arr[i] > max)
        {
            max = arr[i];
            imax = i;
        }
    }
    cout << max << ' ';
    
    for (int i=k; i<n; ++i)
    {
        if (arr[i] > max || imax < i-k+1)
        {
            max = arr[i-k+1];
            imax = i-k+1;
            for (int j=i-k+2; j<=i; ++j)
            {
                if (arr[j] > max)
                {
                    max = arr[j];
                    imax = j;
                }
            }
        }
        cout << max << ' ';
    }
    cout << '\n';
}
int main(){
  
   int t;
   cin >> t;
   while(t>0) {
      int n,k;
       cin >> n >> k;
       int i;
       int arr[n];
       for(i=0;i<n;i++)
            cin >> arr[i];
       printKMax(arr, n, k);
       t--;
     }
     return 0;
}
```

###Inheritance:

 - **Inheritance Introduction**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


class Triangle{
    public:
       void triangle(){
           cout<<"I am a triangle\n";
       }
};
class Isosceles : public Triangle{
    public:
       void isosceles(){
          cout<<"I am an isosceles triangle\n";
       }
    
    void description(){
          cout<<"In an isosceles triangle two sides are equal\n";
       }
        //Write your code here.
};
int main(){
    Isosceles isc;
    isc.isosceles();
    isc.description();
    isc.triangle();
    return 0;
}
```

 - **Rectangle Area**
```cpp
class Rectangle{
  public:
    
    int width;
    int height;
    
  
    
    void Display(){
        
        cout<<width<<" "<<height<<"\n";
        
    }
    
    
};

class RectangleArea: public Rectangle{
    public:
    
    void Input(){
        
        cin>>width;
        cin>>height;
        
    }
    
      void Display(){
        
        int area;
        
          area=width*height;
          
          cout<<area;
          
        
    }
    
    
};
```

 - **Multi Level Inheritance**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

class Triangle{
   public:
      void triangle(){
         cout<<"I am a triangle\n";
      }
};

class Isosceles : public Triangle{
     public:
        void isosceles(){
          cout<<"I am an isosceles triangle\n";
        }
};

   
class Equilateral : public Isosceles{
     public:
        void equilateral(){
          cout<<"I am an equilateral triangle\n";
        }
};

int main(){
  
    Equilateral eqr;
    eqr.equilateral();
    eqr.isosceles();
    eqr.triangle();
    return 0;
}
```

 - **Accessing Inherited Functions**
```cpp
class D: protected A,B,C
{

	int val;
	public:
		//Initially val is 1
		 D()
		 {
		 	val=1;
		 }


		 //Implement this function
		 void update_val(int new_val)
		 {
            int a = new_val;
            while ( a %2 == 0)
          {
               a = a/2;
               A::func(val);
          }
             
           while ( a % 3 == 0)
          {
         a = a/3;
         B::func(val);
          }
             
         while ( a % 5 == 0)
          {
         a = a/5;
         C::func(val);
         }
			
		 }
		 //For Checking Purpose
		 void check(int); //Do not delete this line.
};
```
##Algorithm Domain

###Warmup:

 - **Solve Me First**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int solveMeFirst(int a, int b) {
  return a+b;
}
int main() {
  int num1, num2;
  int sum;
  cin>>num1>>num2;
  sum = solveMeFirst(num1,num2);
  cout<<sum;
  return 0;
}
```

 - **Simple Array Sum**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main(){
    int n;
    int sum=0;
    cin >> n;
    vector<int> arr(n);
    for(int arr_i = 0;arr_i < n;arr_i++){
       cin >> arr[arr_i];
    }
    
    for(int arr_i = 0;arr_i < n;arr_i++){
       sum+= arr[arr_i];
    }
    
    cout<<sum;
    
    return 0;
}
```

 - **A Very Big Sum**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main(){
    int n;
    cin >> n;
    
    long long int sum=0;
    
    vector<int> arr(n);
    for(int arr_i = 0;arr_i < n;arr_i++){
       cin >> arr[arr_i];
    }
    
     for(int arr_i = 0;arr_i < n;arr_i++){
       sum+= arr[arr_i];
    }
    
    cout<<sum;
    
    
    return 0;
}
```

 - **Diagonal Difference**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main(){
    int n;
    cin >> n;
    int diag_a =0;
    int diag_b =0;
    int result;
    
    vector< vector<int> > a(n,vector<int>(n));
    for(int a_i = 0;a_i < n;a_i++){
       for(int a_j = 0;a_j < n;a_j++){
          cin >> a[a_i][a_j];
       }
    }
    
    int k=0;
    int l=n-1 ;
        
    for(int i =0; i<n; ++i){
        diag_a += a[i][k];
        diag_b += a[i][l];
        k++;  
        l--;
    }
    
    result = abs(diag_a-diag_b);
    
    cout<<result;
    
    
    return 0;
}
```

 - **Plus Minus**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main(){
    int n;
    float pos= 0.0f;
    float neg = 0.0f;
    float zero = 0.0f;
    float pos_part, neg_part, zero_part;
    cin >> n;
    vector<float> arr(n);
    for(int arr_i = 0;arr_i < n;arr_i++){
       cin >> arr[arr_i];
        
       if      (arr[arr_i] > 0) {pos++;}
       else if (arr[arr_i] < 0) {neg++;}
       else if (arr[arr_i]==0)  {zero++;}
    }
    
    pos_part = pos/n;
    neg_part = neg/n;
    zero_part = zero/n;
    
    cout<<pos_part<<"\n";
    cout<<neg_part<<"\n";
    cout<<zero_part;
    
    return 0;
}
```

 - **Staircase**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main(){
    
    int n, space, hash;
    cin>>n;
    
for( int i = 0; i<n; i++)
{
    space = (n-1)-i;
    hash = i+1; 
    while(space != 0)
    {
        cout<<" ";
        space--;
    }
    while( hash!= 0 )
    {
        cout<<"#";
        hash--;
    }
    cout<<"\n";

}
    return 0;
}
```

 - **Time Conversion**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <stdio.h>
#include <string.h>
using namespace std;

int main() {
    int hh, mm, ss ;
    char t12[2];
    scanf("%d:%d:%d%s", &hh, &mm, &ss, t12) ;

    if (strcmp(t12,"PM")==0 && hh!=12) hh += 12 ;
    if (strcmp(t12,"AM")==0 && hh==12) hh = 0 ;

    printf("%02d:%02d:%02d", hh, mm, ss) ;
    return 0;
}
```
###Implementation:

 - **Angry Professor**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <string>
using namespace std;

int main(){
    
    vector<string> results;
    int t;
    cin >> t;
    
    for(int a0 = 0; a0 < t; a0++){
        
        int count = 0;
        int n;
        int k;
        cin >> n >> k;
        
        vector<int> a(n);
        
        for(int a_i = 0;a_i < n;a_i++){
          
            cin >> a[a_i];
            if(a[a_i] <=0) {count++;}
        }
        
        if(count >= k) {results.push_back("NO");}
        else           {results.push_back("YES");}
        
    }
    
    for(int i = 0; i < results.size(); ++i){
        
        cout<<results[i]<<"\n";
        
    }
    
    return 0;
}
```

 - **Sherlock and The Beast** (Editorial read, not counting for the score)
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <bits/stdc++.h>

using namespace std;

int main()
{
    int n,test,k,kstart;
    scanf("%d",&test);
    while(test--)
    {
        scanf("%d",&n);
        string ks;
        for(int j=n;j>=0;j--)
        {
            if(j%3==0 && (n-j)%5==0)
            {
                ks="";
                for(int k=0;k<j;k++)
                    ks+='5';
                for(int k=0;k<n-j;k++)
                    ks+='3';
                break;
            }
        }
        if(ks=="")
            cout<<"-1\n";
        else
            cout<<ks<<endl;
    }
    return 0;
}
```

 - **Utopian Tree**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main(){
    int t;
    cin >> t;
    vector<int>results;
    
    for(int a0 = 0; a0 < t; a0++){
        
        int height = 1;
        bool is_spring = true;
        int n;
        cin >> n;
        
        for(int i = 0; i<n; ++i)
            {
            
            if(is_spring)
            {
                height = height*2;
                is_spring = false;
            }
            
            else    
            {
                
                height= height+1;
                is_spring = true;
            }
            
        }
        
        results.push_back(height);
        
    }
    
    for(int i = 0; i<results.size(); ++i){
        
        cout<<results[i]<<"\n";
    }
    
    return 0;
}
```

 - **Find Digits**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

int main(){
    int t;
    cin >> t;
    vector<int>results;
    
    for(int a0 = 0; a0 < t; a0++){
        int n;
        int temp;
        int digit;
        int count = 0;
        cin >> n;
        temp = n;
        
        while(n) {
                        digit = n % 10;
                       
                        n = n/10;
                      
                       if(digit!=0 && temp%digit == 0) {count++;}
                   }
        
        results.push_back(count);
    }
    
    for(int i=0;i<results.size();++i){
        
        cout<<results[i]<<"\n";
        
    }
    
    return 0;
}
```

 - **Sherlock and Squares**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
   
    int t;
    cin >> t;

    
    for(int a0 = 0; a0 < t; a0++){
        int a;
        int b;
        int count = 0;
        cin >> a >> b;
        int range;
        
        for(range = a; range <=b; ++range){
            
            
           int temp = sqrt(range);
            
            if(temp*temp == range)
            
            {
                
                count++;
                range += temp*2 ;
            }
            
          
            
        }
        
      
        cout<<count<<"\n";
    }
    
  
    return 0;
}
```

 - **Cut the sticks**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

int main(){
    int n;
    cin >> n;
    vector<int> arr(n);
    vector<int> new_arr;
    
    for(int arr_i = 0;arr_i < n;arr_i++){
       cin >> arr[arr_i];
    }
    
    while(arr.size()>0){
    sort(arr.begin(),arr.end());
    
    
    for(int i = 0; i<arr.size();++i){
        
        int temp = arr[i] - arr[0];
        
        if(temp > 0){new_arr.push_back(temp);}
        
    }
    
    int cut = arr.size() - new_arr.size();
        
    cout<<new_arr.size() + cut <<"\n";
    
    arr.clear();
    arr = new_arr;
    new_arr.clear();
        
    }
    
    return 0;
}
```

 - **Chocolate Feast**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

int main(){
    int t;
    cin >> t;
    for(int a0 = 0; a0 < t; a0++){
        int n;
        int c;
        int m;
        int bought = 0;
        int exchanged = 0;
        int extra = 0;
        int extra_of_extra = 0;
        int final_extra = 0;
        int final_final_extra = 0;
        int extra_of_extra_of_extra=0;
        int total = 0;
        int leftover = 0;
        
        cin >> n >> c >> m;
        
        bought = n/c;
        
        exchanged = bought/m;
        
        leftover = bought%m;
        
        if(exchanged + leftover >= m){
            
        extra = (exchanged + leftover)/m;
        if (extra>=m) {extra_of_extra = extra%m;}
            
        }
        
         if(extra + extra_of_extra >= m){
            
            final_extra = (extra + extra_of_extra)/m;
            if (final_extra>=m) {extra_of_extra_of_extra = final_extra%m; }
            
        }
        
        
        final_final_extra = (final_extra + extra_of_extra_of_extra)/m;
            
        total = bought+exchanged+extra+final_extra + final_final_extra ;
        
        cout<<total<<"\n";
          
    }
    return 0;
}
```

 - **Cavity Map**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <string>
using namespace std;


int main(){
    int n;
    string number;
    cin >> n;
    
    int** grid = new int*[n];
    for(int i = 0; i < n; ++i) {grid[i] = new int[n];}
    
    char** grid2 = new char*[n];
    for(int i = 0; i < n; ++i) {grid2[i] = new char[n];}
    
   for(int i = 0; i < n; i++){
       
       cin>>number;
    
    for (int j = 0; j < n; j++)
       {
        
              grid[i][j] = (int)number[j];
       }
   }
      
    for(int i=0; i < n; i++){
        for(int j = 0; j<n; j++){
            
        grid2[i][j] =  (char)grid[i][j];     
             
            
     if(i > 0 && i < (n-1) && j > 0 && j < (n-1)){
           
     if (grid[i][j] > grid[i - 1][j] && grid[i][j] > grid[i+1][j] && grid[i][j] > grid[i][j - 1] && grid[i][j] > grid[i][j+ 1] )
         
           {grid2[i][j] = 'X';}
       }
            
        }
    }
    
    for(int i=0; i < n; i++){
        for(int j = 0; j<n; j++){
            
       cout << grid2[i][j];
        
       
            
        }
        
      cout<<endl;
    }
       
    delete grid;
    delete grid2;
    
    return 0;
}
```

 - **Taum and B'day**
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

int main(){
    int t;
    cin >> t;
    for(int a0 = 0; a0 < t; a0++){
        int b;
        int w;
        long long int cost = 0;
        cin >> b >> w;
        long long int x;
        long long int y;
        long long int z;
        cin >> x >> y >> z;
        

        
        if(x > y && (y*b + b*z) < (x*b)) {
        
            cost = (w*y +  y*b + b*z);
        }
                
        else if(y > x && (x*w + w*z) < (y*w)){
        
            cost = (x*b + x*w + w*z);
        }
        
        else {cost = x*b + y*w;}
        
         cout<<cost<<endl;
        
    }
    return 0;
}
```

##CREDITS


Mircea for helping with a few challenging problems.






