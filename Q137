#include <stdio.h>

enum Week {
    MONDAY,
    TUESDAY,
    WEDNESDAY,
    THURSDAY,
    FRIDAY,
    SATURDAY,
    SUNDAY
};

int main() {
    enum Week day;

    const char *names[] = {
        "MONDAY", "TUESDAY", "WEDNESDAY",
        "THURSDAY", "FRIDAY", "SATURDAY", "SUNDAY"
    };

    printf("Enum Names and Their Values:\n");

    for (day = MONDAY; day <= SUNDAY; day++) {
        printf("%s = %d\n", names[day], day);
    }

    return 0;
}
