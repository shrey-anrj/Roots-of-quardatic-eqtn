#include<stdio.h>
#include<math.h>
void main()
{
    double d,a,b,c,r1,r2,realPart,imagPart;
    printf("Enter the coficient of a,b,c: \t");
    scanf("%lf %lf %lf", &a, &b, &c);
    d=b*b-(4*a*c);
    if(d>0)
    {
        r1 = (-b + sqrt(d)) / (2 * a);
        r2 = (-b - sqrt(d)) / (2 * a);
        printf("root1 = %.2lf and root2 = %.2lf", r1, r2);
    }
    else if(d==0)
    {
        r1 = r2 = -b / (2 * a);
        printf("root1 = root2 = %.2lf;", r1);
    }
    else
    {
        realPart = -b / (2 * a);
        imagPart = sqrt(-d) / (2 * a);
        printf("\nroot1 = %.2lf+%.2lfi and \nroot2 = %.2f-%.2fi", realPart, imagPart, realPart, imagPart);
   
    }
}
