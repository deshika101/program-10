# program-10
10. Haunted
The king of ghosts is really disappointed when he sees that all the human beings on
Planet Earth have stopped fearing the ghost race. He knows the reason for this. The
existing ghost race has become really lazy and has stopped visiting Planet Earth to
scare the human race. Hence, he decides to encourage the entire ghost race into
scaring the humans by holding a competition. The king, however, never visits Planet
Earth.
This competition will go on for N days. Currently, there are a total of M ghosts (apart
from the king) existing in the ghost race such that :
- The youngest ghost is 1 year old.
- The oldest ghost is M years old.
- No two ghosts have the same age.
- The age of each and every ghost is a positive integer.
On each day of the competition, ghosts have to visit Planet Earth to scare people. At
the end of each day, a "Ghost of the Day" title is awarded to the ghost who scares the
most number of humans on that particular day. However, the king of ghosts believes
in consistency. Once this title has been given, the ghost who has won the most
number of such titles until that particular moment is presented with a "Consistency
Trophy". If there are many such ghosts, the oldest among them is given the trophy.
Note that this "Title Giving" and "Trophy Giving" happens at the end of each day of
the competition.
You will be given the age of the ghost who won the "Ghost of the Day" title on each
day of the competition. Your job is to find out the age of the ghost who was awarded
with the "Consistency Trophy" on each day of the competition.


#include<bits/stdc++.h>
using namespace std;
int main()
{
int n,m;
cin>>n>>m;
int arr[n];
map<int,int>res;
int max1=0;
int val=0;
for(int i=0;i<n;i++)
{
cin>>arr[i];
if(res.find(arr[i])==res.end())
res[arr[i]]=1;
else
res[arr[i]]++;
if(i==0)
{
cout<<arr[i]<<" "<<res[arr[i]]<<endl;
val=arr[i];
max1=res[arr[i]];
}

else
{
if(max1==res[arr[i]] and arr[i]>val)
{
val=arr[i];
}
else if(res[arr[i]]>max1)
{
val=arr[i];
max1=res[arr[i]];
}
cout<<val<<" "<<max1<<endl;
}

}

}
