def check(num,k):
  if num%3==0:
    return True 
  
def divisible(arr,k):
  i=0 
  num=0 
  while(i<k):
    num=num*10+arr[i] 
    i+=1 
  if (check(num,k)):
    return 0 
  for j in range(i,len(arr)): 
    num=num%(pow(10,k))+arr[j] 
    if (check(num,k)):
      return j-k+3
  return -1 
arr=list(map(int,input().split()))
k=int(input()) 
ans=divisible(arr,k)
if (ans==-1):
  print(-1) 
else:
  for i in range(ans,ans+k):
    print(arr[i],end=" ") 
