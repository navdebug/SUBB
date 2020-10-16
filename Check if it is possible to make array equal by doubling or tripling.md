def check(arr):
  n=len(arr)
  for i in range(n):
    if (arr[i]%2==0):
      arr[i]=int(arr[i]/2) 
    if (arr[i]%3==0):
      arr[i]=int(arr[i]/3) 
  for i in range(n):
    if(arr[i]!=arr[0]):
      return False 
  return True 
arr=list(map(int,input().split())) 
print("yes" if check(arr) else "NO") 
