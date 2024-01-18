#include <iostream>
#include <cmath>
#include <iomanip>

using namespace std;

int main()
{
	int val1 = 0, val2 = 0, result, choice;
	string str("WELCOME TO MATHCULATOR!");
	string str1("MENU");

	do {
		cout << setw(32.5) << str << endl;
		cout << setfill('=') << setw(40) << "=";
		cout << setw(32.5) << str1 << endl;
		cout << setfill('=') << setw(40) << "=";
		cout << "\n[0] - Exit \n[1] - Add \n[2] - Substract \n[3] - Multiplication \n[4] - Divide \n[5] - Modulo \n[6] - Power\n";
		cout << setfill('=') << setw(40) << "=";
		cout << "\n\nEnter your choice: ";
		cin >> choice;
		system("cls");

		cout << setfill('=') << setw(40) << "=";

		if (choice == 0) { //exit
			cout << "\nGoodbye, Pepito my friend.";
			system("exit");
		}
		else {
			cout << "\nInvalid input.";
			continue; //go back to the start of the loop
		}

		cout << "Enter a first value: ";
		cin >> val1;

		cout << "\nEnter a second value: ";
		cin >> val2;
		cout << setfill('=') << setw(40) << "=";

		switch (choice) {

		case 1:
			result = val1 + val2;
			break;

		case 2:
			result = val1 - val2;
			break;
		case 3:
			result = val1 * val2;
			break;
		case 4:
			result = val1 / val2;
			break;
		case 5:
			result = val1 % val2;
			break;
		case 6:
			result = pow(val1, val2);
			break;
		
		cout << "\nResult: " << result;

		default:
			cout << "\nInvalid input.";
		}

	//	cout << "Enter a first value: ";
	//	cin >> val1;

	//	cout << "\nEnter a second value: ";
	//	cin >> val2;
	//	cout << setfill('=') << setw(40) << "=";

	//if (choice == 1) {
	//	result = val1 + val2;
	//}
	//else if (choice == 2) {
	//	result = val1 - val2;
	//}
	//else if (choice == 3) {
	//	result = val1 * val2;
	//}
	//else if (choice == 4) {
	//	result = val1 / val2;
	//}
	//else if (choice == 5) {
	//	result = val1 % val2;
	//}
	//else if (choice == 6) {
	//	result = pow(val1, val2);
	//}
	//else {
	//	cout << "Invalid input.";
	//}

	//cout << "\nResult: " << result;

		return 0;
	} while (choice != 0);
}
