#include <stdbool.h>

bool cse_islower(char c) {
    return c >= 'a' && c <= 'z';
}

void cse_strupper(char str[]) {
    for (int i = 0; str[i] != '\0'; i++) {
        if (cse_islower(str[i])) {
            str[i] = str[i] - ('a' - 'A'); // Convert to uppercase
        }
    }
}
    
    printf("Original string: %s\n", testStr);
    cse_strupper(testStr);
    printf("Uppercase string: %s\n", testStr);
    
    // Test cse_islower function
    printf("Testing cse_islower:\n");
    printf("Is 'a' lowercase? %s\n", cse_islower('a') ? "true" : "false");
    printf("Is 'Z' lowercase? %s\n", cse_islower('Z') ? "true" : "false");
    printf("Is 'm' lowercase? %s\n", cse_islower('m') ? "true" : "false");
    printf("Is '1' lowercase? %s\n", cse_islower('1') ? "true" : "false");

    return 0;
}
