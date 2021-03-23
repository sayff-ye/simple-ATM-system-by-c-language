#include <stdio.h>
#include <stdlib.h>
#include<conio.h>
       /* ATM Program */
       int p,f,c,m,w,d;// matric pin,fast cash,Choice,money,withdraw,Deposit
int sh;

  void file(){
	   
FILE * the_file = fopen("ATM UTHM.txt","a"); //READ FILE
	fprintf(the_file,"\n\t*THE CURRENT BALANCE IS = %d*",m);
	if(the_file==NULL ){
		perror("Unable to open the file ");
		exit(1);
	}
	char line [10];
	while(fgets(line,sizeof(line),the_file)){
		printf("%s",line);
    
}
};
       void menu(){
       	
	 printf("\n\t*****");
     printf("\n\t* Welcome to UTHM Banking Services  *");
     printf("\n\t*           MENU                    *");
     printf("\n\t*     1. Withdraw                   *");
     printf("\n\t*     2. Check Balance              *");
     printf("\n\t*     3. Fast Cash                  *");
     printf("\n\t*     4. Deposit                    *");
     printf("\n\t*                                   *");
     printf("\n\t*****");
     printf("\n\n\t\t"); 
       	
       	
	   };
	   
	   
	   void choose(){
	   	
	   			switch(f){
		
	case 1:{
	if(100 < m)
	{
	printf("\tplease take your cash 100\n\n *Thank You for using our Bank*");
	}
	m-=100;
		break;
	}
		case 2:{
			if(500 < m)
			
	{
	printf("\tplease take your cash 500\n\n *Thank You for using our Bank*");
	}
		m-=500;

			break;
		}
			case 3:{
				if( 2000 < m)
	{
	printf("\tplease take your cash 2000\n\n *Thank You for using our Bank*");	
	}
			m-=2000;

				break;
			}
			case 4:{
				if( 5000 < m)
	{
	printf("\tplease take your cash 5000\n\n *Thank You for using our Bank*");
	}
			m-=5000;;

				break;
			}
			
	default :
		{
				 printf("\tInvalid fast cash option!! \n\t");
break;

		}
}
	   };
int main(void)
{

system("COLOR A0");

m = 10000;
printf("\n\n");
     printf("\n\t*****");
     printf("\n\t* Welcome to UTHM Banking Services  *");
     printf("\n\t* Enter your 5 Digit Matric number: *");
     printf("\n\t*****");
     printf("\n\n\t\t");

     scanf("%d",&p);
if(p==200326)
{
	system("cls");
		system("COLOR 90");


	do{
	menu();
	 scanf("%d",&c); 
	 switch(c){
	 	case 1:{

	printf("\tPlese enter withdraw amount:\n\t");
	scanf("%d",&w);
	if(w < m && w%10==0)
	printf("\tPlease Take your Amount = %d\n",w);
	printf("\n\tYour Current Balance: %d\n\t*Thank You for using our Bank*",m-w);
m=m-w;
			break;
		 }
		 
		 case 2:{
		 	
	printf("\tYour available Amount = %d",m);	
			break;
		 }
		 
		 case 3:{
		 	
	
		 	printf( "\t1->100\n\t2->500\n\t3->2000\n\t4->5000\n\t");
	printf("Please choose fast cash options:\n\t");
	scanf("%d",&f);
	
	choose();

	break;
}
	

	

	
 
	case 4:{
		
	printf("\n\tEnter the amount of Deposit: ");
	scanf("%d",&d);
	printf("\n\tYour Current Balance=%d",m+d);	
	m+=d;
		break;
	}	 
	 default :
  {
   printf("Enter Valid Choice\n");
   break;
  }	 
}
 printf("\n\n~To Continue Press 1 else any mumber to end--->~");
 fflush(stdin);
 scanf("%d",&sh);
   }while(sh==1);
	 }
	 else {
	 	printf("Wrong pin number");
	 }
	    printf("**Thanks for using our ATM**");		 
getch();
file();
	 return 0;
	
	}
