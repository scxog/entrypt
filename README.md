# entrypt

#include <stdio.h>
int main(){
	char lst[100];
	for(;;){
		printf("加密前：");
		fgets(lst,100,stdin);
		for(int i=0;lst[i] != NULL;i++){
			if(65<=lst[i] && lst[i]<=90){
				lst[i]++;
				if(lst[i]>90)
					lst[i] -= 26;
			}
			if(97<=lst[i] && lst[i]<=122){
				lst[i]++;
				if(lst[i]>122)
					lst[i]-=26;
			}
		}
		printf("加密后：%s",lst);
	}
	return 0;
}
