def product(arr):
  length=0 
  prod=1 
  N=len(arr)
  for i in arr:
    prod*=i 
  if (prod>=0):
    return N 
  for i in range(N):
    if arr[i]<0:
      length=max(length,max(i,N-i-1)) 
  return length 
arr=list(map(int,input().split()))
N=len(arr)
r=product(arr)
print(r)
