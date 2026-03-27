# Pat1-subtask2#include <iostream>
using namespace std;

int main() { 
    int temp1, temp2, temp3;

    // Input
    cout << "Enter first temperature reading: ";
    cin >> temp1;

    cout << "Enter second temperature reading: ";
    cin >> temp2;

    cout << "Enter third temperature reading: ";
    cin >> temp3;

    // Check increase from first to second
    if (temp2 - temp1 > 50) {
        cout << "Reduce heat before taking next reading" << endl;
    }

    // Check increase from second to third
    if (temp3 - temp2 > 50) {
        cout << "Reduce heat before taking next reading" << endl;
    }

    // Check small increase overall
    if (temp3 - temp1 < 10) {
        cout << "Oil temperature increase too small" << endl;
    }

    // Final condition (example safe range: 150–190)
    if (temp3 >= 150 && temp3 <= 190) {
        cout << "Oil is ready for frying" << endl;
    } else {
        cout << "Oil is not ready for frying" << endl;
    }

    return 0;
}
