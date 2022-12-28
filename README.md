## Muzero Hex agent
A Muzero model to play Hex board game. Muzero is a genearl algorithm. It works for any games. I build Hex board game environment for it and trained it for 15 hours.

### Model Structure
<img width="893" alt="Screenshot 2022-12-28 at 20 17 44" src="https://user-images.githubusercontent.com/105564219/209867504-eed00df0-6f9b-4054-be46-1df1fac10930.png">
https://rdcu.be/ccErB

There are three deep neural networks.
<br> <b>network h</b> is a representation network. It convert a acutual game board into a matrix which can be fed into a network
<br> <b>network g</b> is a dynamic network. It simulate a next move in the game during MCTS (Monte Carlo Tree Search)
<br> <b>network f</b> is a prediction network. It predict volues and policy for the next move.

### Result
Because Muzero uses MCTS for self-play, it's very slow (takes about 2min to finish one game with 50 rollout). It's very expensive to train a strong AI agent to play Hex. 
<br> I only trained it for 15 hours to have a taste of this state of the art reinforcement learning algorithm.
<br>
<img width="369" alt="Screenshot 2022-12-15 at 00 11 09" src="https://user-images.githubusercontent.com/105564219/209868653-0ca6541e-843a-41c2-bb64-c0a7a79b79b8.png">
<img width="498" alt="Screenshot 2022-12-09 at 12 23 49" src="https://user-images.githubusercontent.com/105564219/209868660-1f725e20-2eea-4f0e-b921-01e91f01602e.png">
Here are two games in which Muzero plays against a random player.
As you can see, sometimes it does makes good moves to connect the two sides. Most of the time it makes waste moves. However, this shows that our Muzero agent surely is learning. It requires much higher computation performance and longer training time.
