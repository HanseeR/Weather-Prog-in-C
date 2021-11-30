# Weather-Prog-in-C
//creating a simple weather program 

//2d array and a weather program , 
//Output : Total rainfall for each year , the average yearly and the average rainfall for each month 
//Input will be 2d ARRAY WITH hard coded values of the rainfall , amounts past 5 years
//should have 5 rows (yrs) and 12 coloumns(months) and the rainfall amounts to the floating points 
//Hints : for loop and the inner for loop , and to calculate the monthly averages
//> Initilize the 2D arrays with the hard-coded rainfall amoounts 
//Project weather 

#include<stdio.h>
#include<conio.h>
#define MONTHS 12
#define YEARS 5

int main()
{
    //Initilaize the rainfall data for 2011-2015
    float rain [YEARS] [MONTHS] =  
    {
        {2.9,3.9,4.8,7.8,2.9,3.9,4.8,7.8,2.9,3.9,4.8,7.8},
        {2.9,3.9,4.8,7.8,2.9,3.9,4.8,7.8,2.9,3.9,4.8,7.8},
        {2.9,3.9,4.8,7.8,2.9,3.9,4.8,7.8,2.9,3.9,4.8,7.8},
        {2.9,3.9,4.8,7.8,2.9,3.9,4.8,7.8,2.9,3.9,4.8,7.8},
        {2.9,3.9,4.8,7.8,2.9,3.9,4.8,7.8,2.9,3.9,4.8,7.8} //dummy repeated variable to save time 
    };
    
    int year , month;
    float subtotal , total , t;
    
    printf("YEAR\t\tRAINFALL       (inches)\n");
    
    for (year = 0, total = 0; year < YEARS; year ++)
    {
        for(month = 0 , subtotal =0; month < MONTHS ; month++)
        {
            subtotal += rain[year][month]; 
        }
        printf("%5d \t\t%15.1f\n", 2010 + year , subtotal);
        total += subtotal;
        
    }
    
 printf("\n The yearly average is %.lf inches.n\n",total/YEARS );
    return 0;
    
}







