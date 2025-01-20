int main() {
    int choice;

    do {
        system("cls"); // Clear screen for a fresh menu display
        showMenu();
        printf("\nEnter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                checkBalance();
                break;
            case 2:
                depositMoney();
                break;
            case 3:
                withdrawMoney();
                break;
            case 4:
                exitATM();
                break;
            default:
                printf("\nInvalid choice! Please select a valid option.\n");
        }

        printf("\nPress any key to return to the menu...\n");
        getchar(); getchar(); // Wait for user input before returning to the menu
    } while (choice != 4);

    return 0;
}

void exitATM() {
    printf("\nThank you for using our ATM simulator. Goodbye!\n");
}
