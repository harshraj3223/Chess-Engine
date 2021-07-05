# Chess-Engine
Team Project (Electronics Club)- Prediction of best possible chess moves for given chessboard layouts using Convolutional Neural Networks.

In the paper '[Reference (Res Paper)](https://github.com/harshraj3223/Chess-Engine/blob/main/Reference%20(Res%20Paper).pdf)', a total of seven different CNNs have been trained for building a chess engine module. The first CNN is for predicting the square from where a move has to be made. The other six CNNs predict the possibility of each of the six distinct pieces in chess (considering white's turn) to go to a particular position as a move.

In our project, we have considered the idea of providing training to just two CNNs, which shall perfectly suffice. The first CNN (The_From_Network) is for predicting an occupied square from where a move should be made, and the second CNN (The_To_Network) is for predicting a blank square, which would get occupied with the move. Moreover, unlike the reference paper, we have also considered including those board layouts in our dataset which call for black's turn. And, to not let those instances sabotage the final results of testing, the layout of the board for each of those cases was augmented as if it called for white's turn. After all of this, we finally got to train the models for around a million different one-hot-encoded chess boards, extracted from the 'FICS_Database.pgn' database, using an extra RAM.

*In the published paper: test/validation accuracies of CNNs: {38.3%}, {52.20%, 29.25%, 56.15%, 40.54%, 26.52%, 47.29%}.*

*In our project: test/validation accuracies of CNNs: {48.65%}, {27.23%}.*

