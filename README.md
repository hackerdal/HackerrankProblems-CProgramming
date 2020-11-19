# HackerrankProblems-CProgramming
Bitwise Operations problem in hackerrank
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>
//Complete the following function.


void calculate_the_maximum(int n, int k) {
    int xor,or,and;
    int maxor=0;
    int maxxor,maxand=0;
    int a,b;
   
    for(a=1 ; a<=n ; a++)
    {
        for(b=1 ; b<=n ; b++)
        {
            if(a<b)
            {
                and=a&b;
            
            
            if(and>maxand && and<k)
            {
                maxand=and;
            }
            or=a|b;
            if(or>maxor && or<k)
            {
                maxor=or;
            }
            xor=a^b;
            if(xor>maxxor && xor<k)
            {
                maxxor=xor;
            }
            
        }
            }
            
    }
    printf("%d\n%d\n%d",maxand,maxor,maxxor);
    
  //Write your code here.
}

int main() {
    int n, k;
  
    scanf("%d %d", &n, &k);
    calculate_the_maximum(n, k);
 
    return 0;
}
