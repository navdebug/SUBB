from math import gcd 
def check(arr,k):
  N=len(arr)
  for i in range(N-k+1):
    g=arr[i]
    for j in range(i+1,i+k):
      g=gcd(g,arr[j]) 
      print(g,end=" ")
arr=list(map(int,input().split()))
k=int(input())
check(arr,k) 
