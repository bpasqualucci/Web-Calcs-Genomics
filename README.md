# Web-Calcs-Genomics
def diaf():  #converts values from diameter to area
	return (3.14*(int(input())/2)**2)
print("Enter plate diameter")
dia1=diaf()
print("Enter plaque diameter")
dia2=diaf()
print("Enter volume added")
sola=int(input())
print("Enter dilution factor")
dfac=int(input())
print("Enter #PFU")
pfu=int(input())

pfum=dia1/dia2
titer=(((pfu/sola)*1000)*10**abs(dfac))
vol=pfum/titer

print("Titer is:",titer)
print("Volume is:",vol)
print("PFUmaxweb is:",pfum)

print()
def conv(): #Converts the volumes to vaules between 10-100, there's prob an easier way to do this....
    
    if vol<10**-12:
        vol2=vol*10**14
        print(vol2,"mL","From -14")
    elif vol<10**-11:
        vol2=vol*10**13
        print(vol2,"mL","From -13")
    elif vol<10**-10:
        vol2=vol*10**12
        print(vol2,"mL","From -12")
    elif vol<10**-9:
        vol2=vol*10**11
        print(vol2,"mL","From -11")
    elif vol<10**-8:
        vol2=vol*10**10
        print(vol2,"mL","From -10")
    elif vol<10**-7:
        vol2=vol*10**9
        print(vol2,"mL","From -9")
    elif vol<10**-6:
        vol2=vol*10**8
        print(vol2,"mL","From -8")
    elif vol<10**-5:
        vol2=vol*10**7
        print(vol2,"mL","From -7")
    elif vol<10**-4:
        vol2=vol*10**6
        print(vol2,"mL","From -6")
    elif vol<10**-3:
        vol2=vol*10**5
        print(vol2,"mL","From -5")
    elif vol<10**-2:
        vol2=vol*10**4
        print(vol2,"mL","From -4")
    elif vol<10**-1:
        vol2=vol*10**3
        print(vol2,"mL","From -3")
    elif vol<10**0:
        vol2=vol*10**2
        print(vol2,"mL","From -2")
    elif vol<10**1:
        vol2=vol*10**1
        print(vol2,"mL","From -1")
    else:
        vol2=vol
        print(vol2,"mL","From 0")

print("/4")
vol=vol/4
div4=conv()

print("/2")
vol=vol*2
div2=conv()

print("Maxweb")
vol=vol*2
mw=conv()

print("X2")
vol=vol*2
tt=conv()

print("X4")
vol=vol*2
tf=conv()

vol=vol/4 #converts the vol value back to its original if needed again

