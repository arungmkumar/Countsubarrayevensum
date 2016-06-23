# Countsubarrayevensum
To count the no of sub arrays with even sum in an integer array


#include <iostream>

using namespace std;


int FindNumber(int arr[],int n){

int count=0;

for(int i=0;i<n;i++){
  int sum=0;
//if(arr[i]%2 == 0 && arr[i]!=1)
if(arr[i]%2 == 0 )
    count++;
    sum+=arr[i];

  for(int j=i+1;j<n&&i<n-1;j++)
  {
      sum+=arr[j];
     if(sum%2 == 0)
        count++;
  }

}
return count;
}

int main(){
int arr[]={1, 2, 2, 3, 4, 1};

int n=sizeof(arr)/sizeof(arr[0]);

cout<<"no of arrays is : "<<FindNumber(arr,n);
return 0;
}
