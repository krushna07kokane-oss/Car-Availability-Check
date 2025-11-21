# Car-Availability-Check
#include <stdio.h>

struct car {
    char name[50];
    int number;
};

int main() {
    struct car c[2];
    int car_number;
    printf("Total Cars List:\n");
    printf("1.Baleno No:8074\n");
    printf("2.Swift No:2345\n");
    printf("3.scorpio No:5678\n");
    

    for (int i = 0; i < 2; i++) {  
        printf("\nCar%d\n", i + 1);  
        printf("Enter car name: ");  
        scanf(" %s", c[i].name);  
        printf("Enter car number: ");  
        scanf("%d", &c[i].number);  
    }  

    printf("\nEnter car number to check availability: ");  
    scanf("%d", &car_number);  

    int i;  
    for (i = 0; i < 2; i++) {  
        if (c[i].number == car_number) {  
            printf("\nCar is AVAILABLE.\n");  
            printf("Car Name: %s\n", c[i].name);  
            break;    
        }  
    }  

    if (i == 2) {
        printf("\nCar is not availabel now\n");
    }

    return 0;
}
