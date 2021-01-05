# ISN-T-IT-A-PANGRAM-
This Python program will check if your sentence is a Pangram
def pandgram(a):
    check='abcdefghijklmnopqrstuvwxyz'
    list1=[]
    k=[]
    r=list(a)
    r.sort()
    s=r.count(" ")
    for i in range(s):
        r.remove(" ")
    for item in range(len(r)):
        list1.append(r[item].lower())
    list1.sort()
    for i in range(len(list1)):
        if(list1[i] in k):
            i=i+1
        else:
            k.append(list1[i])
    grouped=''.join(k)
    if(grouped==check):
        return True
    else:
        return False
        
    
input=str(input('Enter your sentence'))    
print(pandgram(input))
