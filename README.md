NAME:Mohamed Mustafa Hussain
212224240091
REG NO:
# EX 2 : Bresenham‘s Line Drawing Algorithm

**AIM :**

 To  implement the Bresenham’s  algorithm for line using a c coding.

**ALGORITHM :**

   Step 1 : Start.
   
   Step 2 : Initialize the graphics header files and functions.

   Step 3 : Declare the required variables and functions.

   Step 4 : Get the four points for drawing a line namely x1,x2,y1,y2.

   Step 5 : Draw the line using the algorithm.

   Step  6 : Display the output.

   Step 7 : stop.

**Program :**
initgraph(&gd, &gm, "C:\\Turboc3\\BGI");  // Path may vary in your setup

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

**Output :**

![437687696-fa205f12-8cc0-470c-857b-4248b485781e](https://github.com/user-attachments/assets/215cb83d-5ed5-4b87-b55a-9ebe24b63dff)


**Result :**
The Bresenham’s line drawing algorithm was successfully implemented in C. The line was accurately drawn between the given points using efficient pixel plotting.

