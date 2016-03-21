#Advanced Game Programming – Assignment 1: Obtaining 400 points on Hackerrank

Hackerrank nickname: eliodeb

Hackerrank profile link:  http://www.hackerrank.com/eliodeb

Domains, points and current rank:
-	 C/C++

 Points: **571**

 Rank:   **161**

-	Algorithm (solved in C++)

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
##CREDITS


Mircea for helping with a few challenging problems.






