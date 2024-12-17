#include <iostream>
#include <string>
using namespace std;
int roll;

char marks(int earned_marks) {
    char grade;
    if (earned_marks >= 90) {
        grade = 'A';
    } else if (earned_marks >= 80) {
        grade = 'B';
    } else if (earned_marks >= 70) {
        grade = 'C';
    } else if (earned_marks >= 60) {
        grade = 'D';
    } else {
        grade = 'F';
    }
    cout << "Grade earned by "<< roll <<" is: " << grade << endl;
    return grade;
}

int main() {
    string* response1 = new string;
    int* ans = new int(0);
    int marks_earned;
    cout<<"Which user is trying to log in?\n";
    cout<<"Please select and enter one option.\n";
    cout<<"1.Teacher\n";
    cout<<"2.Parent\n";
    cout<<"3.Student\n";
    cin>>*response1;

    if(*response1=="1"||*response1=="teacher"||*response1=="t"||*response1=="T") {
        *ans=1;
    } else if(*response1=="2"||*response1=="parent"||*response1=="p"||*response1=="P") {
        *ans=2;
    } else if(*response1=="3"||*response1=="student"||*response1=="s"||*response1=="S") {
        *ans=3;
    }

    switch(*ans) {
        case 1: {
            cout<<"Welcome teacher, let's get started.\n";
            string* response2 = new string;

            cout<<"Would you like to take attendance first? (Yes/No)\n";
            cin>>*response2;

            if(*response2=="Yes"||*response2=="yes"||*response2=="Y"||*response2=="y") {
                cout<<"Please enter the students' roll numbers (type 'end' to stop):\n";
                string* attendance = new string;
                int* count = new int(0);

                while(true) {
                    cin>>*attendance;
                    if(*attendance=="end") {
                        break;
                    }
                    (*count)++;
                }

                cout<<"Number of students present today: "<<*count<<"\n";

                delete attendance;
                delete count;
            } else {
                cout<<"Please Update the marks for students Exams."<<endl;
                cout<<"Please Enter the roll number of the students' mid-term marks.\n";
                cin>>roll;
                cout<<"Please enter the marks earned by this student";
                cin>>marks_earned;
                marks(marks_earned);
                
            }

            delete response2;
            break;
        }
        case 2: {
            cout<<"Welcome Parent!\n";
            string* response3 = new string;
            cout<<"please enter your childs roll number";
            cin>>roll;
            cout<<"Would you like to check your child's grades or fees?\n";
            cout<<"Enter 1 for Grades and 2 for Fees\n";
            cin>>*response3;

            if(*response3=="1") {
                cout<<"Your child's grades are as follows:\n";
                cout<<"Math: 85\n";
                cout<<"Science: 90\n";
                cout<<"English: 88\n";
            } else if(*response3=="2") {
                cout<<"Your child's fees status: Paid\n";
            } else {
                cout<<"Invalid selection, please restart the program.\n";
            }

            delete response3;
            break;
        }
        case 3: {
            cout<<"Welcome student!\n";
            string* rollNumber = new string;
            string* response2 = new string;
            
            cout<<"Please enter your roll number: ";
            cin>>*rollNumber;
            cout<<"Enter 1 for Grades and 2 for Fees\n";
            cin>>*response2;

            if(*response2=="1") {
                string subjects[] = {"Math", "Science", "English", "History", "Computer Science"};
                int marks[] = {85, 90, 88, 92, 95};

                cout << "Your grades are as follows:\n";
                for(int i = 0; i < 5; i++) {
                    cout << subjects[i] << ": " << marks[i] << "\n";
                }
            } else if(*response2=="2") {
                cout<<"Your fees are paid.\n";
            } else {
                cout<<"Invalid selection, please restart the program.\n";
            }

            delete rollNumber;
            delete response2;
            break;
        }
        default: {
            cout<<"Invalid selection, please restart the program.\n";
            break;
        }
    }

    delete response1;
    delete ans;

    return 0;
}
