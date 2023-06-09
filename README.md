//mini program for atm machine
#include<stdio.h>
int main()
{
    float total_amount,transfer,deposite,withdraw,check_balance;
    int pin,password,user_input;
    printf("Enter the password to enter your account");
    scanf("%d",&password);
    printf("Enter amount to create your account");
    scanf("%f",&total_amount);
    printf("Enter the 1 for check balance \n2.Enter 2 for deposite\n3.Enter for 3 withdraw \n4.Enter 4 for check balance");
    scanf("%d",&user_input);
    printf("Enter pin\n");
    scanf("%d",&pin);
    if(pin==password){
        switch(user_input){
            case 1:
            printf("Your toatal balance in your amount is %f",total_amount);
            break;
            case 2:
            printf("Enter amount to deposite\n");
            scanf("%f",&deposite);
            float net_balance_after;
            net_balance_after=total_amount+deposite;
            printf("The balance after deposite is %f",net_balance_after);
            case 3:
            printf("Enter amount to withdraw\n");
            scanf("%f",&withdraw);
            float balance_after_withdraw;
            balance_after_withdraw=total_amount-withdraw;
            printf("Amount after withdraw is %f",balance_after_withdraw);
            case 4:
            printf("Enter amount to transfer\n");
            float balance_after_transfer=total_amount-transfer;
            printf("Net balance after transfer is %f",balance_after_transfer);
            break;
            default:
            printf("Enter valid user input\n");
            break;
        }

        }
        else{
            printf("Your password is wrong.SO repeat the process\n");
            
        }
        return 0;
    }


