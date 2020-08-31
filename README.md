#include<stdio.h>

void Balance(void);
void Withdraw(void);

int AB;
int WA;


int main()
{
    int c;

printf("Available Balance: ");
scanf("%d",&AB);
printf("Withdrawal Amount: ");
  scanf("%d",&WA);


printf("\n\n Balance Enquiry: 1\n\n Cash Withdraw: 2 \n\n \n Enter Choice: ");
scanf("%d",&c);

switch(c)
{
case 1:
Balance();
break;

case 2:
Withdraw();
break;

default:
printf("Invalid Entry");
}
}

void Balance(void)
{
printf("Available balance is: Rs %d", AB);
}


void Withdraw(void)
{
   if(AB >= WA)
   {
    printf("\n Opening Balance is: Rs %d", AB);

    AB = AB - WA;
   printf("\n Amount Withdrawn is: Rs %d", WA);
    printf("\n Remaining Balance is: Rs %d", AB);
   printf("\n Your Transaction Successful");
   }
   else
   {
   printf("\n Insufficient balance, \n Transaction declined");
   }

}
