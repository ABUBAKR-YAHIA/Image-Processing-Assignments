# 4 and 8 Neighburs
import numpy as np
axis = int(input("Enter the radius of the matrix:"))
neighbor = int(input("Enter the 4 or 8 to calculate the neighbors"))

if neighbor == 4 or neighbor == 8:
    x =np.empty((axis,axis))
    y = np.empty((axis+2,axis+2))
    s =np.empty((axis,axis))
    
    # Generating the Values of the Matrix
    for i in range(0,axis):
        for j in range(0,axis):
            x[i][j]=int(i+j+1)
    for i in range(0,axis):
        for j in range(0,axis):
            print(int(x[i][j]),end = '\t')
        print('\n')


    for i in range(0,axis+2):
        for j in range(0,axis+2):
            if i == 0 or i == axis+1 or j == 0 or j==axis+1:
                y[i][j]=0
            else:
                y[i][j]=x[i-1][j-1]
    for i in range(0,axis+2):
        for j in range(0,axis+2):
            print(int(y[i][j]),end = '\t')
        print('\n')

    for i in range(0,axis):
        for j in range(0,axis):
            if neighbor == 4:                
                s[i][j]=((y[i][j+1]+y[i+1][j]+y[i+1][j+2]+y[i+2][j+1]))
                print(x[i][j],":",end = '\t')
                print(y[i][j+1],',',y[i+1][j],',',y[i+1][j+2],',',y[i+2][j+1])
                #print(s[i][j],end = '\t')
            elif neighbor ==8:
                    s[i][j]=((y[i][j]+y[i][j+1]+y[i][j+2]+y[i+1][j]+y[i+1][j+2]+y[i+2][j]+y[i+2][j+1]+y[i+2][j+2]))
                    print(x[i][j],":",end = '\t')
                    print(y[i][j],',',y[i][j+1],',',y[i][j+2],',',y[i+1][j],',',y[i+1][j+2],',',y[i+2][j],',',y[i+2][j+1],',',y[i+2][j+2])
                    #print(s[i][j],end = '\t')
        print('\n')
else:
     print("Wrong neighbors, you have to select ether 4 or 8")
