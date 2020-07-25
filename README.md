#include <iostream>
#include <algorithm>
using namespace std;

void array (int *integers)
{   
    /*getting user input*/
    cout << "Please enter the elements of an array" << endl;

    for (int i=0; i<10; i++)
    {
        cin >> integers[i];
    }
    
    /*printing an initial array*/
    cout<<"Unsorted array elements:"<<"  ";

    for (int i=0; i<10; i++)
    {
        cout << integers[i] << "  ";
    }
}

int main ()
{
    /*passing the array to the function*/
    int integers[10];
    array (integers);
    
    /*finding the largest number*/
    int max = integers[0];

    for (int i=1; i<10; i++)
    {
        if(integers[i] > max)
        {
            max = integers[i];
        }
        
        int element = max;
        int max_index;
        if(element = integers[i])
        {
            max_index = i;
            cout << "\nThe largest number is: "<< max <<" "<<"["<<i<<"]"<<endl;
        }
    }
    /*finding the smallest number*/
    int min = integers[0];

    for (int i=1; i<10; i++)
    {
        if(integers[i] < min)
        {
            min = integers[i];
        }
        
        int element = min;
        int min_index;
        if(element = integers[i])
        {
            min_index = i;
            cout << "\nThe smallest number is: "<< min <<" "<<"["<<i<<"]"<<endl;
        }
    }
    /*sorting elements into descending order*/
    int n = sizeof(integers)/sizeof(integers[0]); 
    sort (integers, integers+n, greater<int>() ); 
    cout << "Sorted array elements: " << "  ";
    for (int i = 0; i < n; ++i) 
        cout << integers[i] << " "; 
    return 0;
}


