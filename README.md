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
else if (response1 == "student" || response1 == "s" || response1 == "S") {
        ans = 2;
    }    
    
    
    
    

    switch(ans){
        
    case 1:
    cout<<"Welcome teacher, lets get started"<<endl;
    string response2;
    cout<<"would you like to take attendance first?"<<endl;
    cin>>response2;
   if (response2 == "Yes" || response2 == "1" || response2 == "Y" || response2 == "y" || response2 == "yes") {
    cout << "Please enter the students' roll numbers (type 'end' to stop):" << endl;
    string attendance;
    int sum=0;
    while (true) {
        cin >> attendance; 
        sum = sum+1;
        if (attendance == "end") { 
            break; 
        }
    }
    cout<<sum<<" Students are present in class today."<<endl;
}

     else if (response2 == "No" || response2 == "0" || response2 == "n" || response2 == "N" || response2 == "no" || response2 == "NO"){
      cout<<" Please update the students mid terms marks ?"<<endl;
      string response3;
      
      
         
     }    
    break;

    
    
    
    
    
    
    
    }
    
    
    
    
    
    system("pause");
}
