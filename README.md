//  Created by Javid Alasgarli on 12/6/21.
//

#include <iostream>
#include <string.h>
#include <cstdlib>

using namespace std;

void drawing(int draw);

int main() {
    string word;
    int draw = 1;
    string words[22] = {"ass", "fuck", "damn", "dickhead", "shit", "bitchell", "bitch", "asshole", "loser", "jerk", "bottom", "cock", "screw", "slut", "whore", "hooker", "shitass", "cocksucker", "harlot", "streetwalker", "bullshit", "gay"};
    int randomword;
    randomword = rand()%22;
    word = words[randomword];
    string answer;
    cout << "\t\t\t\tWelcome To My Game, Bitch\n";
    cout << "\t\t\t*********************************\n";
    cout << "the word list:\n";
    cout << "ass\tfuck\tdamn\tdickhead\tshit\tbitchella\tbitch\tasshole\tloser\tjerk\tbottom\tcock\tscrew\tslut\twhore\thooker\tshitass\tcocksucker\tharlot\tstreetwalker\tbullshit\tgay\n" << endl;
    cout << "guess the right word: ";
    cout << endl;
    while(draw <= 8) {
        drawing(draw);
        cout << "guess the word: ";
        cin >> answer;
        cout << endl;
        if(answer == word) {
            cout << "\n\nCongratulations!!! You guessed my word.\n\n" << endl;
            break;
        } else {
            cout << "\n\nTry it out again\n\n";
            draw++;
        }
        randomword = rand()%22;
    }
    
    return 0;
}

void drawing(int draw) {
    if(draw==1) {
        cout << "\t_________\n\t|\t |\n\t|\t 0\n\t|\t/|\\" << "\n\t|\t |\n\t|\t/ \\\n\t|__" << endl;
    } else if(draw == 2) {
        cout << "\t_________\n\t|\t |\n\t|\t 0\n\t|\t/|\\" << "\n\t|\t |\n\t|\t/ \n\t|__" << endl;
    } else if(draw == 3) {
        cout << "\t_________\n\t|\t |\n\t|\t 0\n\t|\t/|\\" << "\n\t|\t |\n\t|\t \n\t|__" << endl;
    } else if(draw == 4) {
        cout << "\t_________\n\t|\t |\n\t|\t 0\n\t|\t/|\\" << "\n\t|\t \n\t|\t \n\t|__" << endl;
    } else if (draw == 5) {
        cout << "\t_________\n\t|\t |\n\t|\t 0\n\t|\t/|" << "\n\t|\t \n\t|\t \n\t|__" << endl;
    } else if(draw == 6) {
        cout << "\t_________\n\t|\t |\n\t|\t 0\n\t|\t/" << "\n\t|\t \n\t|\t \n\t|__" << endl;
    } else if(draw == 7) {
        cout << "\t_________\n\t|\t |\n\t|\t 0\n\t|\t" << "\n\t|\t \n\t|\t \n\t|__" << endl;
    } else if(draw == 8) {
        cout << "\t_________\n\t|\t |\n\t|\t \n\t|\t" << "\n\t|\t \n\t|\t \n\t|__" << endl;
    }
    
}
