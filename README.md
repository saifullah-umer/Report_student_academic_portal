#include <iostream>
using namespace std;

int main() {
    string *response1=new string;
    int *ans=new int(0);
    cout<<"Which user is trying to log in?"<<endl;
    cout<<"Please select and enter one option."<<endl;
    cout<<"1. Teacher"<<endl;
    cout<<"2. Parent"<<endl;
    cout<<"3. Student"<<endl;
    cin>>*response1;
    if(*response1=="teacher"||*response1=="t"||*response1=="T"){
        *ans=1;
    }else if(*response1=="parent"||*response1=="p"||*response1=="P"){
        *ans=3;
    }else if(*response1=="student"||*response1=="s"||*response1=="S"){
        *ans=2;
    }    
    switch(*ans){
        case 1:{
            cout<<"Welcome teacher, let's get started."<<endl;
            string *response2=new string;
            cout<<"Would you like to take attendance first?"<<endl;
            cin>>*response2;
            if(*response2=="Yes"||*response2=="1"||*response2=="Y"||*response2=="y"||*response2=="yes"){
                cout<<"Please enter the students' roll numbers (type 'end' to stop):"<<endl;
                string *attendance=new string;
                int *sum=new int(0);
                while(true){
                    cin>>*attendance;
                    if(*attendance=="end"){
                        break;
                    }
                    (*sum)++;
                }
                cout<<"Number of students present today: "<<*sum<<endl;
                delete attendance;
                delete sum;
            }else if(*response2=="No"||*response2=="0"||*response2=="n"||*response2=="N"||*response2=="no"||*response2=="NO"){
                cout<<"Please update the students' mid-term marks."<<endl;
            }
            delete response2;
            break;
        }

    case 2:
        cout << "Welcome student!" << endl;
        
        cout << "Please enter your roll number: ";
        cin >> rollNumber;

        cout << "Enter 1 for Grades and 2 for Fees" << endl;
        cin >> response2;
    
    
    }
    
    case 3: 
        cout << "Welcome Parent!" << endl;
        string response3;
        cout << "Would you like to check your child's grades or fees?" << endl;
        cout << "Enter 1 for Grades and 2 for Fees" << endl;
        cin >> response3;
        
        if (response3 == "1") {
            cout << "Your child's grades are as follows:" << endl;
            cout << "Math: 85" << endl;
            cout << "Science: 90" << endl;
            cout << "English: 88" << endl;
        } else if (response3 == "2") {
            cout << "Your child's fees status: Paid" << endl;
        } else {
            cout << "Invalid selection, please restart the program." << endl;
        }
        break;
    
    
    
    system("pause");
}
