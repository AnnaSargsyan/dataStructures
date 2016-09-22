/* Data Structures HW
 Anna Avanesyan
 Anna Sargsyan */


#include <iostream>
#include <algorithm>

using namespace std;




void findingMinimum( int number, int array[]){
   
    
    for(int n=0; n < number ; n++){
        int minimum = n;
        for(int i = n; i < number ; i++){
            if(array[i] < array[minimum]){
                minimum = i;
            }
        }
        
        swap(array[minimum], array[n]);

    }
    
}


int main(){
    
    int number;
    int array[number];
    
    cout<< "Enter the number of elements" << endl;
    cin>> number;
    cout << "Enter the list of elements" << endl;
    
    for(int i=0; i< number;i++){
        cin >> array[i];
    }
    
    findingMinimum(number, array);
    
    for(int i=0; i< number; i++){
        cout << array[i] << " " ;
    }
    
    return 0;
}
    
