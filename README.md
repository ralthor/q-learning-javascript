# Simple Q-learning implementation using javascript
This is a small implementation of Q-learning using Javascript.

## Q-Learning story
The learning process in Q-Learning is based on scoring the next possible actions. These are called Q-values. It means looking at the environment during the learning process, the agent scores each of its actions based on its experience. For example, in a maze game, such as PacMan, if some actions lead the agent to win the game, the scores of those actions are increased to increase their chance to be selected later. On the other hand, if some actions lead to fail, for example running into a ghost, the scores are decreased to avoid selecting them in the future.

## Implementation notes:
- To develop Q-Learning, I make a big loop over all of the episodes I want to have, which could be unlimited.
- Inside that loop, I put the agent in the starting state, and let it react to the environment based on its Q-values.
- When the agent reaches to the end of the current episode (either by reaching a final state or the end of its permitted action numbers), I make a list out of its state, action pairs.
- To avoid loops inside the list of state, action pairs, the actions which create a loop is not selected.
- Starting from the end of the list, I apply the learning formula to all of the state, action pairs it traversed.
- Instead of adding the reward, I simply multipied it. It helps not to be aware of reducing it while going backward through the list.

I have written a [post here](https://blog.communere.com/A-Brief-Description-on-Q-Learning) about this implementation.
