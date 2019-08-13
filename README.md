# Ubercode
# Uber car direction finding after moving some distance in any direstion.


#include <stdio.h>
#include <stdlib.h>

//int timecalc();

int main()
{
    int x=0;
    int y=0;
    int laps;
   // int time=0;
    int s;
   // int T;
    int D;   //D is distance ex) 10,20,20..
    char d;   //d is direction ex) N,E,W and S.
    scanf("%d\n",&laps);
    for(int i;i<laps;i++)
    {
        scanf("%d %d %c",&D,&s,&d);  //enter distance then press space bar and enter the direction

        if((d=='N')||(d=='S')||(d=='W')||(d=='E'))
        {
            if(d=='N')
                y=D+y;
            if(d=='S')
                y=-D+y;
            if(d=='E')
                x=D+x;
            if(d=='W')
                x=-D+x;
        }

     }

     if((x==0)||(y==0))
     {
         if((x==0)&&(y>0))
            printf("N");
         if((x==0)&&(y<0))
            printf("S");
         if((x>0)&&(y==0))
            printf("E");
         if((x<0)&&(y==0))
            printf("W");
     }
     else{
        if((x>0)&&(y>0))
            printf("NE");
        if((x<0)&&(y<0))
            printf("WS");
        if((x<0)&&(y>0))
            printf("WN");
        if((x>0)&&(y<0))
            printf("SE");
     }
     return 0;
}




/*
//sample input:

     3
     10 N
     20 W
     14 E



 //Expected output

     WN

 */

