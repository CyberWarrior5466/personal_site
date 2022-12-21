<!-- Q5 dastan wiki https://en.wikibooks.org/wiki/A-level_Computing/AQA/Paper_1/Skeleton_program/2023#Question_5 -->

1. At the beginning of the game allow each player to enter their own name instead of `Player One` or `Player Two`  

   <details>
     <summary>View Solution</summary>
   
     ```python
     class Dastan:
       def __init__(self, R, C, NoOfPieces):
           self._Board = []
           self._Players = []
           self._MoveOptionOffer = []
           self._Players.append(Player(input("Player One enter name: "), 1))
                                     # ++++++++++++++++++++++++++++++++
           self._Players.append(Player(input("Player Two enter name: "), -1))
                                     # ++++++++++++++++++++++++++++++++
           ...
     ```
   </details><br>


2. Add a new move called `TibbleCross`. This move allows a piece to move up two spaces diagonally.
  
-  This move should appear first in the queue

-  To test this move the piece from the co-ordinate "22" to "44" 
    
   $\def\arraystretch{1.5}
   \begin{array}{|c|c|c|c|c|}
   \hline
   \mathrm{X} & \ \ \ & \ \ \ & \ \ \ & \mathrm{X} \\ \hline
              &       &       &       &            \\ \hline
              &       &   *   &       &            \\ \hline
              &       &       &       &            \\ \hline
   \mathrm{X} &       &       &       & \mathrm{X} \\ \hline
   \end{array}$

