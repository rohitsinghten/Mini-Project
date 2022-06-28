# Mini-Project
//Name - Rohit Singh              Mini Project (Electricity bill)
//Roll no- RA211027010183
#include <stdio.h>
int main()
{
    int unit;
    float amt, total_amt, service_charge;
    printf("Enter total units consumed: ");
    scanf("%d", &unit);
    /* Calculate electricity bill according to given conditions */
    if(unit <= 50)
    {
        amt = unit * 0.50;
    }
    else if(unit <= 150)
    {
        amt = 25 + ((unit-50) * 0.75);
    }
    else if(unit <= 250)
    {
        amt = 100 + ((unit-150) * 1.20);
    }
    else
    {
        amt = 220 + ((unit-250) * 1.50);
    }
     /*
     * Calculate total electricity bill
     * after adding surcharge */
    service_charge = amt * 0.20;
    total_amt  = amt + service_charge;
    printf("Electricity Bill = Rs. %.2f", total_amt);
    return 0;
}
