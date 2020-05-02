---
    title: Devising Your Strategy
---

To play this game, we will be using an open-source, pedagogical software called ‘Oyun’ (pronounced OY-oon) which was created by Charles H. Pence for teaching concepts of evolutionary game theory. Oyun literally means ‘game’ in Turkish.

Oyun allows strategy input in an FSA format written as a.txt file.

<figure>
  <img src="/pd-game/res/oyun.png" alt="oyun.png"/>
  <figcaption>Figure 2: Logo of OYUN- A PD game simulator</figcaption>
</figure>

---

### What’s an FSA?

FSA stands for ‘finite state automata’, and this will be the format that will help the simulator understand our strategy. FSA has ‘states’ which, in our case, represent the moves to play. Counting of states begins from 0. The first move which the strategy plays in the game is the one in state 0. From then on, the ‘reader’ can go to another state via ‘arrows’ connecting them. In our case, the arrows will tell the opponent’s last move.

Here is an example of an FSA showing the TIT FOR TAT strategy - a strategy that has rules like this- ‘Cooperate the first turn and then on mimic the opponent’s last move’.

Keep these rules in mind while designing the automaton for your strategy-

<figure>
  <img src="/pd-game/res/fsa.png" alt="fsa.png"/>
  <figcaption>Figure 3: An FSA diagram depicting the TIT FOR TAT strategy</figcaption>
</figure>

1. Keep numbering your states from 0.
2. Make sure the ‘reader’ always has a state to go to, i.e. each state must have one ‘if the opponent played C then’ and one ‘if the opponent played D then’ arrows.
3. We don’t need a ‘final’ state. Just make sure the above rule is completed.
4. Like in the example, you don’t need two separate states for every round. You can always circle back to the same state or go back to the state you’ve been to.
5. The FSA here is a ‘deterministic’ model which means you need to make sure there aren’t two (or more) arrows of the same kind emanating from one state (say State 0 is connected to both State 1 and State 5 with an ‘if C’ arrow).

Remember, a strategy must have a rule since the end of the game is probabilistic. That’s right, with each round, there is a 0.00346 chance of the game to end (Axelrod’s game end probability). With no sure end, making a strategy where every round is accounted for separately is a moot endeavour.

Put on your thinking caps and start cracking!

### Typing up your FSA

Coding out your FSA is a piece of cake for Oyun once you’ve chalked out its design. Follow these steps and make your strategy complete for submission into the tournament! Read up Section 5 to see an example of a strategy.

1. The file to send is a .txt file. You can make one on ‘Notepad’ if using Windows; TextEditor if using macOS and on the Terminal itself if using Linux.
2. In your .txt file, type out the following-
  ```
  Strategy Author
  Strategy Name
  Number of states (N)
  State 0
  State 1
  ...
  State N-1
  ```
  Here, each state information should be given as below-
  `<move>, <next state if opponent moves C>, <next state if opponent moves D>`

  As an example-
  ```
  IISER Mohali
  TIT FOR TAT
  2
  C,0,1
  D,0,1
  ```

3. Check the above example with the FSA diagram given above to get a feel. Your le must have only the aforementioned text and nothing else. Remember, each state MUST be associated with a number and a move to play, i.e. either C or D.

4. And just like this, you have yourself a strategy complete and ready to take part in the tournament!
