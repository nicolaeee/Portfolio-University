---
title: Bubble sort in C++/JavaScript
---


Well as we all know there are a lot of sorting methods in programming, but base is base for everyone and everyone should know not only ease method of sorting an array in JS but also the true technique of bubble sort.

# C++
```
#include <iostream>
using namespace std;

int main()
{
    //Reading the array from the keyboard
    int array[20], m;
    cout<<"Enter numbers of elements: ";
    cin>>m;
    for(int i =0;i<m;i++){
        cout<<"Array ["<<i<<"] =";
        cin>>array[i];
    }
    //Outputing unsorted array
    for(int i =0; i<m;i++){
        cout<<array[i];
    }    cout<<'\n';
    //Bubble Sort method with swap function which sorts the array in the right order
    for(int j =0; j< m-1;j++){
        for(int i = 0; i<m-1;i++){
            if(array[i]>array[i+1]){
                swap(array[i], array[i+1]);
            }
        }
    }
    //Outputing the sorted array with bubble sort
    for(int i =0; i<m;i++){
        cout<<array[i]<<'\n';
    }

}
```
# JavaScript

```
function bubbleSort(array){

    for(var i = 0; i <= array.length-1; i++){
        // Last i elements are already in place
        for(var j = 0; j < ( array.length - i -1); j++){

            // Comparing two adjacent numbers
            // and see if first is greater than second
            if(array[j] > array[j+1]){

            // Swap them if the condition is true
            var temp = array[j]
            array[j] = array[j + 1]
            array[j+1] = temp
            }
        }
    }
    // Print the sorted array
    console.log(array);
}
```
Here is everything so warm and clear