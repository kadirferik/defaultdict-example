# defaultdict-example
from collections import defaultdict
d = defaultdict(list)
v = {}
l = {}
bos = {}
n = input(" ")
m = int(n[2])
p = input()
k = int(n[0])
s = []
lst = []
blst = []
blst1 = []
deger = []
deger1 = []
bos1 = {}
bos2 = {}
for i in range(len(p)):
    s.append(i+1)
for i in p:
    lst.append(i)
for e, r in zip(s, lst):
    bos[e] = r
for i in range(k):
    blst.append(bos[i+1])
for i in range(m):
    blst1.append(bos[i+k+1])
for i in range(k):
    deger.append(i+1)
for i in range(m):
    deger1.append(i+1)
for u, z in zip(deger, blst):
    bos1[u] = z
for x, q in zip(deger1, blst1):
    bos2[x] = q
d["A"] = bos1
d["B"] = bos2
print(d["A"])
print(d["B"])
for i in range(1,k+1):
    if d["A"][i] == d["B"][m-(m-1)]:
        v[i] = (i)
    elif d["A"][i] == d["B"][m-(m-2)]:
        l[i] = (i) 
vlist = list(v.values())        
llist = list(l.values())
for i in range(len(vlist)):
    print(vlist[i] ,end=" ")
print()
for i in range(len(llist)):
    print(llist[i] ,end=" ")
