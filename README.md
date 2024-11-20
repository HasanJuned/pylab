# breshman
import matplotlib.pyplot as plt

# from 9,17 to 13,22

x1,y1 = 9,17
x2,y2= 13,22

dx= x2-x1
dy= y2-y1
p= 2*dy - dx
print(p)

points=[]
points.append((x1,y1))

xi,yi = x1,y1

while xi!=x2 and yi!=y2:
    if p<0:
        xi=xi+1
        p= p + 2*dy
    else:
        xi= xi+1
        yi = yi+1
        p = p+ 2*(dy-dx)


    points.append((xi,yi))

points.append((x2,y2))

x= [point[0] for point in points]
y= [point[1] for point in points]

print(points)

plt.plot(x,y,color='r',marker='o')
plt.show()


# DDA


import matplotlib.pyplot as plt

# from (1,1) to (4,3)

x1,y1= 1,1
x2,y2 = 4,3

dx = x2-x1
dy= y2-y1
m= dy/dx
print(m)

points=[]

points.append((x1,y1))
xi,yi= x1,y1
while xi!=x2 and yi!=y2:
    if(abs(dx)>=abs(dy)):
        xi= xi+1
        yi= yi + m
    else:
        yi=yi+1
        xi= xi+ 1/m


    points.append((xi,yi))

points.append((x2,y2))
print(points)


x = [point[0] for point in points]
y = [point[1] for point in points]

plt.plot(x,y,color='b',marker='o')
plt.grid(True)
plt.show()


# Reflectio

import matplotlib.pyplot as plt

## Reflection among x axis point is (4,5)

x,y = 4,5
x1,y1= x, -y

plt.scatter(x,y,color='b')
plt.scatter(x1,y1,color='r')

# Show only the x and y axis lines
plt.axhline(0, color='black', linewidth=0.8)
plt.axvline(0, color='black', linewidth=0.8)

plt.show()

## Reflection among y axis point is (4,5)
## here is have added label to make the graph look better

x, y = 4, 5
x1, y1 = -x,y

# Create the plot
plt.scatter(x, y, color='b', label='(x, y)')
plt.scatter(x1, y1, color='r', label='(x1, y1)')

# Show only the x and y axis lines
plt.axhline(0, color='black', linewidth=0.8)
plt.axvline(0, color='black', linewidth=0.8)

# Add labels and legend
plt.legend()
plt.show()

#  Mirroring Across Both Axes for point (4,5)

x, y = 4, 5
x1, y1 = -x,-y

# Create the plot
plt.scatter(x, y, color='b', label='(first x, first y)')
plt.scatter(x1, y1, color='r', label='(mirrored x, mirrored y)')

# Show only the x and y axis lines
plt.axhline(0, color='black', linewidth=0.8)
plt.axvline(0, color='black', linewidth=0.8)

# Add labels and legend
plt.legend()
plt.show()

