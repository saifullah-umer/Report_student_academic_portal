//Report_student_academic_portal
#include <iostream>
 using namespace std;
int main() {
    string response1;
    int ans=0;
    
    cout<<"Are you a teacher, a Student or a Parent? "<<endl;
    cout<<"Please select and enter one option."<<endl;
    
    cin>>response1;
    
    if ( response1 == "teacher" || response1 =="t" || response1 =="T"){
        ans = 1;
    }
    
    
    
    
    

    switch(ans){
        
    case 1:
    
    cout<<"Welcome teacher, lets get started"<<endl;
    string response2;
    
    cout<<"would you like to take attendance?"<<endl;
    cin>>response2;
    
    if (response2 == "Yes" || response2 == "1" || response2 == "Y" || response2 == "y" || response2 == "yes" || response2 == "YES"){
    cout<<"Please enter the students roll number: "<<endl;
    }
    else if (response2 == "No" || response2 == "0" || response2 == "n" || response2 == "N" || response2 == "no" || response2 == "NO")
    
    break;
    
    case 2:
    cout<<"welcome student please enter your roll number to fetch your academic record: "
    int reg_num;
    cin>>reg_num;
    
    
    
    }
    
    
    
    
    
    system("pause");
}
