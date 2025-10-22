# tp-02
code 01

#include <stdio.h>
#include <stdlib.h>

char *LoadString(int N) {
    char *str = (char *)malloc((N + 1) * sizeof(char));
    if (str == NULL) {
        printf("Memory allocation failed!\n");
        exit(1);
    }
    printf("Enter your string: ");
    fgets(str, N + 1, stdin);
    return str;
}

int main() {
    int n;
    printf("Enter maximum string size: ");
    scanf("%d", &n);
    getchar();
    char *s = LoadString(n);
    printf("You entered: %s\n", s);
    free(s);
    return 0;
}
