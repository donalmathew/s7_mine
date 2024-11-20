![[Pasted image 20241119191816.png]]

These are AI agents that use knowledge representation and reasoning to make decisions. Think of them as agents that try to understand and act upon the world using a knowledge base (like a database of facts and rules).

![[Pasted image 20241120215145.png]]
![[Pasted image 20241120215221.png]]
![[Pasted image 20241120215230.png]]
![[Pasted image 20241120215239.png]]


Key points about knowledge-based agents:
- They maintain an internal knowledge base (KB) of what they know
- They can update their knowledge through perception
- They use reasoning to derive new facts from existing knowledge
- They use this knowledge to decide what actions to take and act intelligently

For example, imagine a chess-playing AI:
```
Knowledge Base:
- Rules of chess
- Current position of pieces
- Strategies and patterns
- Past game experiences

Reasoning:
IF enemy_queen_threatens_my_king AND safe_square_available
THEN move_king_to_safe_square
```


Structure of a knowledge-based agent:
  1. Knowledge Base (KB): Stores facts about the world
  2. Inference Engine: Derives new facts
  3. TELL: Adds new facts to KB
  4. ASK: Queries the KB
  5. Learning Component: Updates knowledge



Example:
```python
class KnowledgeBasedAgent:
    def __init__(self):
        self.KB = []  # Knowledge Base

    def TELL(self, fact):
        self.KB.append(fact)

    def ASK(self, query):
        return self.infer(query, self.KB)
```

![[Pasted image 20241120200933.png]]
![[Pasted image 20241120200944.png]]
