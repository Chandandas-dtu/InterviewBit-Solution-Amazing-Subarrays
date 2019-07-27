# InterviewBit-Solution-Amazing-Subarrays
bool isvowel(char ch) 

{ 
    
    return (ch == 'a' || ch == 'e' || 
            ch == 'i' || ch == 'o' || 
            ch == 'u'|| ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U'); 
} 

int Solution::solve(string A) 
{  
    
    int n = A.length(), ans=0;
    
    for(int i=0; i<n; i++)
    
    {
        if(isvowel(A[i]))
        {
            for(int len=1; len<=n-i; len++)
                ans++;
        }
    }
    return ans%10003; 
}


