//Basic operations in an array


    #include <stdio.h>

    int main() {  
    //Creating an array
    int LA[]={1,3,5,6,7};
    
    //Traversing the array
    int ele=10,k=3,n=5;
    int i=0,j=n;
    printf("The Array elements are:\n");
    for(i=0;i<n;i++){
        printf("LA[%d]=%d\n",i,LA[i]);
    }
    
    //Inserting an elements in the array
    n=n+1;
    while(j>=k){
        LA[j+1]=LA[j];
        j=j-1;
    }
    LA[k]=ele;
    printf("The Array elements after insertion:\n");
    for(i=0;i<n;i++){
        printf("LA[%d]=%d\n",i,LA[i]);
    }
    
    //Deleting an element 
    j=k;
    while (j<n){
        LA[j-1]=LA[j];
        j=j+1;
    }
    n=n-1;
    printf("The Array elements after deletion:\n");
    for(i=0;i<n;i++){
        printf("LA[%d]=%d\n",i,LA[i]);
    }
    
    //Searching an element in the array 
    while(j<n){
        if(LA[j]==ele){
            break;
        }
        j=j+1;
    }
    printf("Found the element %d at %d\n",ele,j+1);
    
    //Updating an element in an array
    LA[k-2]=ele;
    printf("The array elements after updation:\n");
    for(i=0;i<n;i++){
        printf("LA[%d]=%d\n",i,LA[i]);
    }

    return 0;
    }
