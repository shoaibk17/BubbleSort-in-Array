# BubbleSort-in-Array

#include <iostream>

using namespace std;


int main() {
    int n; std::cin >> n;
    int arr[n];
    
    for(int i = 0; i<n; i++){
        cin>>arr[i];
    } int counter = 0;
	while(counter<n){
   	 for(int i = 0; i<n- counter; i++){
        	if(arr[i]>arr[i+1]){
          	  int temp = arr[i];
          	  arr[i]= arr[i+1];
           	 arr[i+1]= temp;
        }
    }
    counter++;
}
	for(int i = 0; i<n; i++){
        std::cout << arr[i] << std::endl;
    }
}

                                        INSERTION Sorting in ARRAY.
                                        
                                        
 #include <iostream>

using namespace std;
    
int main() {
    int n; std::cin >> n;
    int arr[n];
    
    for(int i = 0; i<n; i++){
        cin>>arr[i];
    }
    for(int i = 1; i<n;i++ ){
        int current = arr[i];
        int j = i-1;
        while(arr[j]>current && j>=0){
            arr[j+1] = arr[j];
            j--;
        }
        arr[j+1] = current;
    }
     
    for(int i = 0; i<n; i++){
        std::cout << arr[i]<<" ";
    }
    cout<<endl;
}

                                        
                                
                                        Longest Arthimetic SubArray 
               
#include <iostream>
using namespace std;

int main() {
    
    int n; std::cin >> n;
    int arr[n];
    
    for(int i = 0; i<n; i++){
        cin>>arr[i];
    }
    int j =2;
    int current = 2;
    int ans = 2;
    int pd = arr[1] - arr[0];
    
    while(j<n){
        if(pd == arr[j] - arr[j - 1]){
            current++;
        }
        else{
            pd = arr[j] - arr[j-1];
            current = 2;
        }
        ans = max(ans, current);
        j++;
    }
    std::cout <<ans<<endl;
	// your code goes here
	return 0;
}

			Smallest Positive Interger in AN ARRAY.
			  
#include <iostream>
using namespace std;

int main() {
    int n; std::cin >> n;
    int arr[n];
    for(int i = 0; i<n; i++){
        cin>>arr[i];
    }
    
    const int N =1e6+2;
    bool check[N];
    for(int i = 0; i<n; i++){
        check[i] = false;
    }
    for(int i=0;    i<n;    i++){
        if(arr[i]>= 0){
            check[arr[i]] = true;
        }
    }
    int ans = -1;
    for(int i =1; i<N; i++){
        if(check[i] == false){
            ans = i;
            break;
        }
    }
    std::cout << ans << std::endl;
	// your code goes here
	return 0;
}
				
				 
				 PAIR SUM of SUB- ARRAY = K
				 
#include <iostream>
#include<climits>
using namespace std;

int PairSum(int arr[], int n, int key){
    int low = 0;
    int high = n-1;
    while(low<high){
        if(arr[low] + arr[high] == key){
            cout<<low<<" "<<high<<endl;
            return true;
        }
        else if(arr[low] + arr[high]> key){
            high--;
        }
        else{
            low++;
        }
    }
    return false;
}

int main() {
   int n; std::cin >>  n;
   int arr[n];
   for(int i = 0; i<n;  i++){
       cin>>arr[i];
   }
   int key; cin>>key;
	cout<<PairSum(arr, n, key)<<endl;
	  
// your code goes here
	return 0;
}

	
				Print Spiral Array
	
	
#include <iostream>
using namespace std;

int main() {
	// your code goes here
	int n,m;
	std::cin >> n>>n;
	int a[n][n];
	
	for(int i = 0; i<n; i++){
	    for(int j = 0; j<n; j++)
	        cin>>a[i][j];
	}
    int rowstart =0, rowend = n-1, columnstart = 0,  columnend = n-1;
    while(rowstart<=rowend && columnstart<=columnend){
        // for rowstart
        for(int col = columnstart; col<= columnend; col++)
            std::cout << a[rowstart][col]<<" ";
        rowstart++;
        
        //for columnend
        for(int row = rowstart; row<= rowend; row++)
            cout<<a[row][columnend]<<" ";
        columnend--;
        
        //for row end;
        for(int col = columnend; col >=columnstart; col--)
            cout<<a[rowend][col]<<" ";
        rowend--;
        
        //for columnstart
        for(int row = rowend; row>= rowstart; row--)
            cout<<a[row][columnstart]<<" ";
        columnstart++;   
    }return 0;
}

				 
				 
