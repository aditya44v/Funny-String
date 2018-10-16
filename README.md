#include <bits/stdc++.h>

using namespace std;

int main()
{
    int q,i,j;
    cin>>q;
    for(i=0;i<q;i++)
    {
        string s;
        cin>>s;
        
        int g=s.length();
        int a[g];
        for(j=0;j<g;j++)
        {
            a[j]=int(s[j]);
            
           
        }
        int b[g];
        for(j=1;j<g;j++)
        {
            b[j]=abs(a[j]-a[j-1]);
            
            
        }
        
      string r;
        r=s;
        reverse(r.begin(),r.end());
        int x[g];
        for(j=0;j<g;j++)
        {
            x[j]=int(r[j]);
            
           
        }
        int z[g];
        for(j=1;j<g;j++)
        {
            z[j]=abs(x[j]-x[j-1]);
           
            
            
        }
       int cnt=0;
      for(j=1;j<g;j++)
       {
          
           if(b[j]==z[j])
           {
              cnt++;
           }
           
       }
      if(cnt==(g-1))
      {
          cout<<"Funny"<<endl;
      }
        else{
            cout<<"Not Funny"<<endl;
        }
    }
   
    return 0;
}
