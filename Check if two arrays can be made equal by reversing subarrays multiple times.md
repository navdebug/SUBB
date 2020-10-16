def check(a,b,n):
  a.sort()
  b.sort()
  for i in range(n):
    if a[i]!=b[i]:
      return False
  return True 
a=list(map(int,input().split())) 
b=list(map(int,input().split()))
n=len(a) 
if(check(a,b,n)):
  print("Yes")
else:
  print("No") 
