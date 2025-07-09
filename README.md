//we use 9 turn cause there is 3 row and coloumn 
for(int turn=0;turn<9;turn++){
board(dis);
//this is optional if you want we can jump code this but our program have a problem
 while(true) {
            cout << "Player " << (currentplayer == player1 ? "1" : "2") << ", enter position (1-9): ";
            
            if(!(cin >> position)) { // If input fails (non-number)
                cin.clear(); // Clear error flag
                cin.ignore(numeric_limits<streamsize>::max(), '\n'); // Discard bad input
                cout << "Please enter a number between 1-9!\n";
                continue;
            }
            
            break; // Valid input
        }

while(position < 1 || position > 9) {
            cout << "Invalid position. Please enter 1-9: ";
            cin >> position;}

 int row = (position - 1) / 3;
  int col = (position - 1) % 3;
  while(dis[row][col] == x || dis[row][col] == o) {
            cout << "Position already taken. Choose another: ";
            cin >> position;
            row = (position - 1) / 3;
            col = (position - 1) % 3; }
  
  dis[row][col]=currentplayer
