# NAME: DEEPIKA G
# REG.NO: 212224040060

# EX 2 : Bresenham‘s Line Drawing Algorithm

## AIM :

 To  implement the Bresenham’s  algorithm for line using a c coding.

## ALGORITHM :

   Step 1 : Start.
   
   Step 2 : Initialize the graphics header files and functions.

   Step 3 : Declare the required variables and functions.

   Step 4 : Get the four points for drawing a line namely x1,x2,y1,y2.

   Step 5 : Draw the line using the algorithm.

   Step  6 : Display the output.

   Step 7 : stop.

## Program :

#include <stdio.h>

#include <conio.h>

#include <graphics.h>

#include <stdlib.h>

#include <math.h>

int main()

   {
     int gd = DETECT, gm;
     int xa, xb, ya, yb;
     int dx, dy, x, y, xend, p;

initgraph(&gd, &gm, "C:\\Turboc3\\BGI");  

printf("Enter the first endpoint (xa, ya): ");

scanf("%d %d", &xa, &ya);

printf("Enter the second endpoint (xb, yb): ");

scanf("%d %d", &xb, &yb);

dx = abs(xb - xa);

dy = abs(yb - ya);

p = 2 * dy - dx;

if (xa > xb) {
    x = xb;
    y = yb;
    xend = xa;
    
} else {
    x = xa;
    y = ya;
    xend = xb;
}

putpixel(x, y, 6);

while (x < xend) {
    x++;
    if (p < 0) {
        p += 2 * dy;
    } else {
        y++;
        p += 2 * (dy - dx);
    }
    putpixel(x, y, 6);
}

getch();

closegraph();

return 0;

## Output :
![Screenshot 2025-04-27 172358](https://github.com/user-attachments/assets/baa35be7-ddbb-4a92-96e0-cb1b6084f8ff)

## Result :
Thus the Bresenham’s algorithm for line using a c coding is implemented successfully.
