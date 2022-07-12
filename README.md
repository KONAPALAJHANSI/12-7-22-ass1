import math
n=1000000
seive=[True]*n 
seive[0]=seive[1]=False
x=int(math.sqrt(n))
for i in range(2,x+1):
    if seive[i]:
        for j in range(i*i,n,i):
            seive[j]=False
t=int(input())
for i in range(t):
    count=0
    n=int(input())
    for i in range(1,n+1):
        if seive[i]:
            count=count+1 
    print(count)
