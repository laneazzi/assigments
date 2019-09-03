// AYEDUN OLANREWAJU//
#include <iostream>
#include <string>
#include <fstream>

using namespace std;
// Creates a struct with objects to hold all the student information//
struct Student
{
    string fname;
    string lname;
    int numGrades;
    int grades[10];
};
// loadclasslist reads info from linked file and loads it into the array of objects//
int loadClassList(Student *classList, string input_data)
{

    ifstream fin;
    fin.open(input_data);
    int i = 0;

    while (!fin.eof())
    {
        fin >> classList[i].fname >> classList[i].lname >> classList[i].numGrades;

        for (int j = 0; j < classList[i].numGrades; j++)
        {

            fin >> classList[i].grades[j];
        }

        i++;
    }

    return i;
}
// Prints the data in the referenced student object//
void printClassList(Student *classList, int classSize)
{
    for (int i; i < classSize;i++)
    {
        cout << classList[i].fname << " "<<""
             << classList[i].lname << " "<<"";

        for (int j = 0; j < classList[i].numGrades; j++)
        {

            cout << classList[i].grades[j]
            <<endl;
        } ;
    }
}

int main()
{
    Student classList[100];
    int classSize = 0;

    classSize = loadClassList(classList, "input_data.txt");

    printClassList(classList, classSize);

    return 0;
}
