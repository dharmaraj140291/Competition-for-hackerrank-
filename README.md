# Competition-for-hackerrank-
import sys
def winner(comp):
    mx=0
    winner=''
    for i in comp:
        v=i[2]-i[1]
        w=i[0]
        if mx<v and mx!=v:
            mx=v
            winner=i[0]
    print(winner,end=" ")
    print(mx)
    
if __name__ == "__main__":
    n = int(input().strip())
    comp=[]
    for a0 in range(n):
        name, d, j = input().strip().split(' ')
        name, d, j = [str(name), int(d), int(j)]
        comp.append([name,d,j])
    winner(comp)
