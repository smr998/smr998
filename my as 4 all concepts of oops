#include <iostream>
#include <string>
#include <fstream>
using namespace std;
// Function
void function()
{
    int n, i;
    int arr[n];
    printf("Enter size of array: ");
    scanf("%d", &n);
    for (i = 0; i < n; i++)
    {
        printf("%d ", arr[i]);
    }
    printf("After reversal: \n");
    for (i = 0; i < n / 2; i++)
    {
        int temp;
        temp = arr[i];
        arr[i] = arr[n - i - 1];
        arr[n - i - 1] = temp;
    }
    for (i = 0; i < n; i++)
    {
        printf("%d ", arr[i]);
    }
}
// Class Object
class student
{
private:
    string name;
    int roll;

public:
    void getdata()
    {
        string ch;
        int n;
        cout << "Enter Name: ";
        cin >> ch;
        ch = name;
        cout << "Enter Roll number: ";
        cin >> n;
        n = roll;
    }
    void display()
    {
        cout << "Name: " << name;
        cout << "Roll Number: " << roll;
    }
};

// friend function

class friend1
{
    private:
    int a,b;
    public:
    friend void friend2(friend1);
    void getdata()
    {
        cout<<"Enter the value of a and b: ";
        cin>>a>>b;
    }
};


void friend2(friend1 f)
{
    cout<<"Sum of a and b: "<<f.a+f.b<<endl;
}
// static member function

class static1
{
    private:
    int a,b;
    public:
    static int c;
    void getdata()
    {
        cout<<"Enter the value of a and b: ";
        cin>>a>>b;
    }
    static void display()
    {
        cout<<"Sum of a and b: "<<c<<endl;
    }
};


int static1::c=0;
// inline function

class inline1
{
    private:
    int a,b;
    public:
    void getdata()
    {
        cout<<"Enter the value of a and b: ";
        cin>>a>>b;
    }
    inline void display()
    {
        cout<<"Sum of a and b: "<<a+b<<endl;
    }
};
// this pointer

class this1
{
    private:
    int a,b;
    public:
    void getdata()
    {
        cout<<"Enter the value of a and b: ";
        cin>>a>>b;
    }
    void display()
    {
        cout<<"Sum of a and b: "<<a+b<<endl;
    }
    void sum(this1 *p)
    {
        cout<<"Sum of a and b: "<<p->a+p->b<<endl;
    }
};
// Inheritance
// Constructor & Destructor
class Parent
{
public:
    Parent()
    {
        cout << "Inside base class" << endl;
    }
    ~Parent()
    {
        cout << "Destructor evoked" << endl;
    }
};
class Child : public Parent
{
public:
    Child()
    {
        cout << "Inside sub class" << endl;
    }
};
// Polymorphism
float area(int r)
{
    float a;
    float pi = 3.14;
    a = pi * r * r;
    return a;
}
int area(int l, int b)
{
    float a1;
    a1 = l * b;
    return a1;
}
float area(int n, int bs, int h)
{
    float a2;
    a2 = n * bs * h;
    return a2;
}
// Template
template <typename T>
T myMax(T x, T y)
{
    return (x > y) ? x : y;
}
// Operator Overloading
class College
{
    int c;

public:
    College()
    {
        c = 0;
    }
    College operator++(int)
    {
        c++;
    }
    int get_c()
    {
        return c;
    }
    College operator--(int)
    {
        c--;
    }
};
// Exception Handling
double division(int a, int b)
{
    if (b == 0)
    {
        throw "Division by zero condition!";
    }
    return (a / b);
}
int main()
{
    int c, n;
    do
    {
        cout << "1. Function\n";
        cout << "2. Class & Object\n";
        cout << "3. friend function\n";
        cout << "4. static member function\n";
        cout << "5. inline function\n";
        cout << "6. this pointer\n";
        cout << "7. Inheritance + Constructor Destructor\n";
        cout << "8. Polymorphism\n";
        cout << "9. Template\n";
        cout << "10. Operator Overloading\n";
        cout << "11. File Handling\n";
        cout << "12. Exception Handling\n";
        cout << "13. Exit\n";
        cin >> n;
        switch (n)
        {
        case 1:
        {
            function();
            break;
        }
        case 2:
        {
            student st;
            st.getdata();
            st.display();
            break;
        }
        case 3:
        {
            friend1 f1;
            f1.getdata();
            friend2(f1);
            break;
        }
        case 4:
        {
            static1 s1;
            break;
        }
        case 5:
        {
            inline1 i1;
            i1.getdata();
            i1.display();
            break;
        }
        case 6:
        {
            this1 t1;
            t1.getdata();
            t1.display();
            t1.sum(&t1);
            break;
        }
        case 7:
        {
            Parent P;
            Child Ch;
            break;
        }
        case 8:
        {
            int b, bs, h, r, l;
            float are;
            cout << "\nEnter the Radius of Circle: \n";
            cin >> r;
            are = area(r);
            cout << "\nArea of Circle: " << are << endl;
            cout << "Enter the Base & Height of Triangle:\n";
            cin >> bs;
            cin >> h;
            are = area(0.5, b, h);
            cout << "\nArea of Triangle: " << are << endl;
            cout << "\nEnter the Length & Breadth of Rectangle: \n";
            cin >> l >> b;
            are = area(l, b);
            cout << "\nArea of Rectangle: " << are << endl;
            break;
        }
        case 9:
        {
            cout << myMax<int>(3, 7) << endl;
            cout << myMax<double>(3.0, 7.0) << endl;
            cout << myMax<char>('g', 'e') << endl;
            break;
        }
        case 10:
        {
            College b;
            cout << "Initial No Of Students " << b.get_c() << endl;
            b++;
            b++;
            b++;
            cout << "Present No Of Students " << b.get_c() << endl;
            b--;
            b--;
            b--;
            cout << "Present No Of Students " << b.get_c() << endl;
            break;
        }
        case 11:
        {
            ofstream MyFile("file.txt");
            MyFile << "Hello, My name is Aditya Bhardwaj.";
            string myText;
            ifstream MyFileRead("file.txt");
            while (getline(MyFileRead, myText))
            {
                cout << myText;
            }
            MyFile.close();
            MyFileRead.close();
            break;
        }
        case 12:
        {
            int x = 50;
            int y = 0;
            double z = 0;
            try
            {
                z = division(x, y);
                cout << z << endl;
            }
            catch (const char *msg)
            {
                cerr << msg << endl;
            }
            break;
        }
        case 13:
        {
            exit(0);
            break;
        }
        }
    } while (c != 13);
    return 0;
}
