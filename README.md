
#include<stdio.h>
void balchecking();
void cashwithdrawl();
void Deposition();
int pins[2][2]={1234,10000,2345,20000}; //Stored pins and balances for checking pin validity.We can add more pin
 int userdet[2]; //for storing user details at run-time 
main()
{
   char op; //op=option
   int a,i;
   printf("Enter your 4-digit  pin:");
   scanf("%d",&a);
      if(a != pins[0][0] &&  a != pins[1][0]) //we can add loop if we have more stored pins
       {printf("You entered wrong pin,Try again\n");
          main();
        }
        if(a==pins[0][0])
         { userdet[0] = a;
         userdet[1] = pins[0][1];
         }
         if(a==pins[1][0])
         { userdet[0] = a;
         userdet[1] = pins[1][1];
         }
      
   printf("Choose any one of the option:\nA.Balance Checking.\nB.Cash Withdrawl.\nC.Cash Deposition\n");
scanf("\n%c",&op);

   switch(op)
   {
    case 'A':
        balchecking();
        break;
    case 'B':
      cashwithdrawl();
      break;
    case 'C':
       Deposition();
      break;
   }
   printf("\n\aThank you for your visit\n");
}
void balchecking()
{
extern int userdet[2];
 printf("Your balance is:%d\n",userdet[1]);
}
void cashwithdrawl()
{
 int b;
   extern int userdet[2];

     printf("Enter the amount to withdrawl:");
     scanf("%d",&b);
    userdet[1]=userdet[1] - b;
     printf("available balance:%d\n",userdet[1]);
   
 } 
 
 void Deposition()
 {
 int d; //to hold the amount to be deposited
 extern int userdet[2];
 printf("Enter the amount to be deposited:");
 scanf("%d",&d);
 userdet[1] = userdet[1] + d;
 printf("Available Balance:%d\n",userdet[1]);
 }
 
 
  
