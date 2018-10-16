# Assignment-2
This is a repository for assignment 2
#include<stdio.h>

#include<stdlib.h>

#include<unistd.h>

#include<sys/wait.h>

int main(){
	
int status=0;
	
int sum=0,sum1=0,sum2=0,sum3=0,sum4=0,sum5=0,sum6=0,sum7=0,sum8=0,sum9=0,sum10=0;
	
int arr[1000];
	
	for(int i=0;i<1000;i++){
	
	arr[i]=i;
	
}
	
int cpid1=fork();
	
if(cpid1==0){
		
for(int i=0;i<100;i++){
	
		sum1=sum1+arr[i];
	
	}
	
}
	
else{
	
	wait(&status);
	
	exit(0);
	
}
	
int cpid2=fork();
	
if(cpid2==0){
		
for(int i=100;i<200;i++){
	
		sum2=sum2+arr[i];
	
	}

	
}
	
else{

	wait(&status);

	exit(0);

	}

int cpid3=fork();

if(cpid3==0){
	
	for(int i=200;i<300;i++){
		
	sum3=sum3+arr[i];
		
      }

	
}

	else{

		wait(&status);
		
                exit(0);
	
            }
	
int cpid4=fork();

if(cpid4==0){

		for(int i=300;i<400;i++){

			sum4=sum4+arr[i];

		}
	
}
	
else{

         wait(&status);

          exit(0);

     }
	
int cpid5=fork();
	
if(cpid5==0){

		for(int i=400;i<500;i++){
			
                sum5=sum5+arr[i];
	
	}
	
}
	
else{
		
     wait(&status);
		
     exit(0);
	
    }   
	
int cpid6=fork();

	if(cpid6==0){
	
	for(int i=500;i<600;i++){

			sum6=sum6+arr[i];

		}
	
}
	
else{
	
	wait(&status);
	
	exit(0);
	
     }

int cpid7=fork();

if(cpid7==0){
		
for(int i=600;i<700;i++){
	
		sum7=sum7+arr[i];
	
	}
	
}
	
else{
	
	wait(&status);
	
	exit(0);

     }
	
int cpid8=fork();
	
if(cpid8==0){
		
for(int i=700;i<800;i++){

                   sum8=sum8+arr[i];
	
	}

}
	
else{
		
        wait(&status);
	
	exit(0);
	
     }
	
int cpid9=fork();
	
if(cpid9==0){
		
for(int i=800;i<900;i++){
	
		sum9=sum9+arr[i];

		}

	}
	

else{

         wait(&status);

	 exit(0);
	
}
	
int cpid10=fork();
	
if(cpid10==0){
		
for(int i=900;i<1000;i++){
	
		sum10=sum10+arr[i];

	  }
	
}
	
else{
		
       wait(&status);
	
	exit(0);
	
}
	
sum=sum+sum1+sum2+sum3+sum4+sum5+sum6+sum7+sum8+sum9+sum10;
	
printf("Final Sum is=");
	
printf("%d",sum);
	
return 0;

}


Ques2:


When a socket is created, the program has to specify the address domain and the socket type. Two processes can communicate with each other only if their sockets are of the same type and in the same domain.


To run the client you need to pass in two arguments, the name of the host on which the server is running and the port number on which the server is listening for connections. 


#include <stdio.h>
#include <sys/types.h>
#include <sys/socket.h>
#include <netinet/in.h>
#include <netdb.h>


void error(char *msg)
{
    perror(msg);
    exit(0);
}

int main(int argc, char *argv[])
{

}
