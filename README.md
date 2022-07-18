#include<stdio.h>
#include<math.h>
struct crcktr{
      char name[50];
      long long int score[5];
    };
int main()
{
    struct crcktr crcktr1,crcktr2;
    scanf("%s",crcktr1.name);
    int i;
    double s = 0,temp=0;
    for(i=0;i<5;i++){
        scanf("%lld",&crcktr1.score[i]);
        s = s + crcktr1.score[i];
    }
    s = s/5;
    for(i=0;i<5;i++){
        temp = temp + (s-crcktr1.score[i])*(s-crcktr1.score[i]);
    }
    temp = sqrt(temp/2);
    scanf("%s",crcktr2.name);
    s = 0;
    double temp2=0;
    for(i=0;i<5;i++){
        scanf("%lld",&crcktr2.score[i]);
        s = s + crcktr2.score[i];
    }
    s = s/5;
    for(i=0;i<5;i++){
        temp2 = temp2 + (s-crcktr2.score[i])*(s-crcktr2.score[i]);
    }
    temp2 = sqrt(temp2/2);
    if(temp>temp2){
        printf("More consistant player is %s",crcktr2.name,temp2,temp);
    }
    else if(temp<temp2){
        printf("More consistant player is %s",crcktr1.name,temp,temp2);
    }
    else{
        printf("Both cricketer are equally consistant");
    }

    return 0;
}

