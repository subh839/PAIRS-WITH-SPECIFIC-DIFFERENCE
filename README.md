# PAIRS-WITH-SPECIFIC-DIFFERENCE

int maxSumPairWithDifferenceLessThanK(int arr[], int n, int k)
    {
        int sum=0;
        sort(arr,arr+n);
        for(int i=n-1;i>0;){
            if(arr[i]-arr[i-1] < k){
                sum += arr[i] + arr[i-1];
                i -= 2;
            }
            else{
                i--;
            }
        }
        return sum; // Your code goes here   
    }
