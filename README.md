# employe-salary
#include <iostream>

using namespace std;
class Employee
{
    int salary[5];
public:
    void accept_details()
    {

        cout<<"enter the salaries of 5 employee"<<endl;
        for (int i=0; i<5; i++)
        {
            cin>>salary[i];
        }
    }
    void display_min()
    {
        int MIN=salary[0];
        for (int i=1; i<5; i++)
        {
            if(salary[i]<MIN)
            {
                MIN=salary[i];
            }

        }
            cout<<MIN<<endl;
    }
    void display_max()
    {int MAX=salary[0];
        for (int i=0; i<5; i++){


            if (salary[i]>MAX)
            {
              MAX=salary[i];

            }
        }
        cout<<MAX<<endl;
    }

};
int main()
{
    int ch;
    Employee s;

while (true)
    { cout<<"Enter the Choice"<<endl;
        cout << "1.employees salary details" << endl;
        cout << "2.Minimum salary" << endl;
        cout << "3.maximum salary" << endl;
        cin>>ch;
        switch(ch)
        {
        case 1:
            s.accept_details();
            break;
        case 2:
            s.display_min();
            break;
        case 3:
            s.display_max();
            break;
        case 5:
            return 0;
        default:
            cout<<"invalid choice"<<endl;


        }

    }

    return 0;
}


