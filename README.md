# NOIP2019
/*2019-06-24*/
//线性筛，利用欧拉函数积性
//p与a互质phi（p*a）=phi（p-1）*phi（a）
//p与a不互质phi（p*a）=phi（p）*phi（a）
  #include<iostream>
  #include<cstdio>
  #define maxn 10000
  bool mark[maxn];
  int prime[maxn],phi[maxn];
  int tot,ans;
  void getphi(int n)
  {
   int i,j;
   phi[1]=1;
   for( i=2;i<=n;i++)
   {
     if(!mark[i])
     {
       prime[++tot]=i;
       phi[i]=1;
      }
      for(j=1;j<=tot;j++)
    {
      if(i*prime[j]>n) break;
      mark[i*prime[j]]=1;
      if(i%prime[j])=0;
      {
        phi[i*prime[j]]=prime[i]*prime[j];break;
       }
       else
       phi[i*prime[j]]=phi[i]*(prime[j]-1);
     }
  }
}
  int main()
  {
  int N;
  cin>>N;
  getphi(N);
  for(int i=1;i<=tot;i++)
  {
                         cout<<prime[i]<<" ";
   }                                       
    cout<<endl;
    return 0;
    }
               
 /*2019-08-05*/
 //数据结构queue
 //FIFO
 #include<queue>
using namespace std;
int main()
{
	queue<int> q;
	q.push(1);
	q.push(2);
	q.push(3);
	cout<<q.front()<<endl;
	q.pop();
	cout<<q.front()<<endl;
	q.pop();
	cout<<q.front()<<endl;
	return 0;
}

  
      
  

