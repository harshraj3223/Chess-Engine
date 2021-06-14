# Chess-Engine
Team Project (Electronics Club)- Prediction of best possible chess moves for given chess board layouts using Convolutional Neural Networks.

In the paper ('Reference (Res Paper).pdf'), a total of seven CNNs are trained. The first CNN for predicting the square from where a move has to be made. The other six CNNs are for predicting the possibility of each of the six distinct pieces in chess (considering white's turn) to go to a particular position as a move.

In our project, we have considered training only two CNNs, which'll perfectly suffice. The first CNN (The_From_Network) is for predicting the square from where a move has to be made. The second CNN (The_To_Network) is for predicting the square to where a move has to be made ( given the board layout in each case ). Moreover, unlike the reference paper, we have also considered including those board layouts in our dataset which call for black's turn. For each of those cases, the layout of the board was augmented in such a way that could make it appear as if it calls for white's turn. 

# In the published paper: test/validation accuracies of CNNs: {38.3%}, {52.20%, 29.25%, 56.15%, 40.54%, 26.52%, 47.29%}.

# In our project: test/validation accuracies of CNNs: {48.65%}, {27.23%}.

