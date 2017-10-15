# ATM-Machine-
#include<stdio.h>
void balchecking();
void cashwithdrawl();
void Deposition();
main()
{
   char op; //op=option
   printf("Choose any one of the option:\nA.Balance Checking.\nB.Cash Withdrawl.\nC.Cash Deposition\n");
   getchar(op);
   switch(op)
   {
    case 'A':
        balchecking();
        break;
    case 'B':
      cashwithdrawl();
      break;
    case 'C':
      Cash Deposition();
      break;
   }
   printf("Thank you for your visit");
}
   
   
