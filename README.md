# Assignment-3
[11:09 am, 8/10/2024] Prathmesh Patil AISSMS : #To Calculate the length of transition curve
V= int(input("Enter the value of design speed: "))
R= int(input("Enter the value of Radius of curvature: "))
N= int(input("Enter the value of slope: "))
W= float(input("Enter the value of width of road including extra widening: "))
emax=float(input("enter the value for plain terain:"))
ecal= (V*V/(225*R))
if ecal < emax:
  print("The value of Super elevation:",ecal)
  print(ecal)
else:
  print(emax)
Ls=(emax*N*W/2)
print("The length of transition curve:", Ls)
[11:09 am, 8/10/2024] Prathmesh Patil AISSMS : #To Calculate the Equivalent Wheel Load (EWL)
R = int(input(" Constant R: "))
C = int (input (" Constant C: "))
A = int(input ("Total Data Values for EWL_Constant: "))
B = int(input ("Total Data Values for AADT: "))
EWL_Constant = []
AADT = []
for i in range (1, A+1):
    print ("Enter EWL Constant:")
    A = float (input())
    EWL_Constant. append(A)
for j in range (1, B+1):
    print ("Enter AADT: ")
    B = float (input ())
    AADT. append (B)
#Calculate the dot product of the two lists
product = sum([x*y for x,y in zip(EWL_Constant, AADT)])
# print(" Dot Product:\n",product)
Total_EWL = product
print (" Total EWL :", Total_EWL)
print ("EWL after 60 years :", Total_EWL*1.6)
TI = 1.35* (((1.6* Total_EWL) + ((product) /2)) ** 0.11)
print ("Traffic Index : ", TI)
Thickness = 0.166*TI* (99-R)/(C**0.2)
print ("Pavement Thickness: ", Thickness, "cm")
[11:09 am, 8/10/2024] Prathmesh Patil AISSMS : P =float (input(" Load in kg: "))
p =float (input (" Tyre pressure kg/cm^2: "))
M = int (input ("Total Number of layers in a given Pavement : "))
pi = 3.14159
CBR = []
for i in range (1, M+1):
    print ("California Bearing Ratio of Material in %")
    CBR_value = float (input ())
    CBR. append(CBR_value)
    T = ((1.75*P)/ (CBR_value) -(P/(p*pi)) ) **0.5
    print ("Thickness Above this layer: ", T, "cm")
print ("Given that bitumen layer of 4 cm")
