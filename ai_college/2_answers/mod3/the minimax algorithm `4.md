![[Pasted image 20241119191517.png]]
![[Pasted image 20241021203224.png]]
![[Pasted image 20241021203148.png]]
![[Pasted image 20241021203420.png]]


#### ALgorithm: ![[Pasted image 20241021210436.png]]
![[Pasted image 20241021210503.png]]
![[Pasted image 20241021210529.png]]

Pseudocode:
![[Pasted image 20241120121227.png]]
![[Pasted image 20241120121239.png]]
#### What is minimax?
- Assumption:
	- Opponent also plays optimally.
- Type:
	- Recursive or backtracking algorithm
	- uses recursion to search through the game tree.
	- proceeds all the way down to the terminal node of the tree, then backtrack the tree as the recursion.
- Search method:
	- DFS
	- performs a depth-first search algorithm for the exploration of the complete game tree.
- used in:
	- Decision making
	- Game theory
		- Chess
		- Checkers
		- TIc-tac-toe

#### Properties:
- Complete:
	- will definitely find a solution(if exists) in finite search tree.
- Optimal
	- if both players play optimallly
- Time complexity:
	- Performs DFS =>O(b^m)
		- b: branching factor
		- m: max depth of search tree
- Space complexity:
	- O(bm)

#### Limitations:
- slow for complex games like chess due to its
	- huge branching factor
		- player has lot of choices

#### Working (search procedure):
- computes the min-max decision for the current state.
- Two players plays the game:
	- MAX
		- selects the maximum value
		- player trying to win
	- MIN
		- selects minimum value
		- opponent who tries to minimise MAXs score.
- MAX moves first and then they take turns until game is over
- in the end
	- points awarded to the winner
	- penalties given to loser

#### search strategy
1. Nodes will be marked to indicate whose turn it is to move or select.
2. terminal states show utility values.
3. Given a game tree, the optimal strategy can be determined by examining the min-max value of each node, which we write as minmax-value (n).
4. The minmax-value of a node is the utility for MAX of being in the corresponding state.


![[Pasted image 20241021214636.png]]
![[Pasted image 20241021214648.png]]
![[Pasted image 20241021214657.png]]
![[Pasted image 20241021214705.png]]
![[Pasted image 20241021214715.png]]
![[Pasted image 20241021214722.png]]






#### Reference notes
![[Pasted image 20241021204418.png]]
![[Pasted image 20241021204642.png]]
