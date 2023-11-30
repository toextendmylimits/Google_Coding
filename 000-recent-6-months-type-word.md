# These questions appear in the past 6 months, so could appear again
## Graph BFS/DFS

Whether a word can be typed from a keyboard  

  Given a 2D keyboard, and a “maximum jump distance” jump_distance, determine if a given word can be constructed using the characters in the keyboard, obeying the jump_distance. A jump can be up, down, right, or left. But NO diagonal, i.e. a diagonal jump would naturally consume 2 units of jump distance. See my answer in post https://leetcode.com/discuss/interview-question/4236648/Google-Phone-Screen/

An important thing to know is whether the keyboard has duplicate letters. Maybe initially the interviewer says that the keyboard doesn't have duplicate letters but then asks to modify the solution to support keyboard having duplicate letters as a follow-up question. Solutions are provided to both scenarios.

  1. Keyboard doesn't have duplicate letters
The idea is to save each letter's position in the keyboard as a pair of x coordinate and y coordinate in a hash map and then check whether the distance between all the adjacent letters is within the jump distance.

<details>

  ```python
   def can_word_be_typed(self, keyboard, word, jump_distance):
       letter_keyboard_positions_map = {}
       for r in range(len(keyboard)):
           for c in range(len(keyboard[0])):
               letter_keyboard_positions_map[keyboard[r][c]] = (r, c)
       
       current_position = None
       for i in range(len(word)):
           next_position = letter_keyboard_positions_map[word[i]]
           if current_position and abs(next_position[0] - current_position[0]) + abs(next_position[1] - current_position[1]) > jump_distance:
               return False
           current_position = next_position
       
       return True
  ```
</details>

     
  2. Keyboard has duplicate letters
This scenario is more complicated and can be solved in approaches of DFS or BFS.

    a. Solve the problem recursively, i.e. DFS
Built on the solution for first scenario, we can still save each letter's positions in the keyboard. However, given there are duplicate letters, now we need to save each letter and all its positions as a list in a hash map. We can define a recursive function to check whether a letter in the word can be typed from a keyboard position.

In each recursive call, we need to know index of the next letter in word to type, and the current keyboard position.
i. If there is no more letter to type, then we know all letters of the word can be typed and return True.
ii. Otherwise we find a position that is within the jump distance to the current position and then check whether the following letter can be typed from the new position.
iii. In the end, return False to indicate the letter can't be typed from current keyboard position.

<details>
  
  ```python
 def can_word_be_typed(self, keyboard, word, jump_distance):
     letter_keyboard_positions_map = defaultdict(list)
     for r in range(len(keyboard)):
         for c in range(len(keyboard[0])):
             letter_keyboard_positions_map[keyboard[r][c]].append((r, c))
     
     def can_letter_be_typed(letter_idx, curr_position):
         if letter_idx == len(word):
             return True
         
         letter = word[letter_idx]
         for next_position in letter_keyboard_positions_map[letter]:
             if curr_position and abs(next_position[0] - curr_position[0]) + abs(next_position[1] - curr_position[1]) > jump_distance:
                 continue
             if can_letter_be_typed(letter_idx + 1, next_position):
                 return True

         return False
     
     return can_letter_be_typed(0, None)
  ```
</details>

b. Solve the problem using BFS
We add the first letter's positions to a queue and record index of the next letter in the word we need to type. Then we do the following things until queue is empty:
i. If there is no more letter to check, return True
ii. We add the letter's positions that are within the jump distance to previous position to the queue, i.e. can be typed from the keyboard
iii. Increase index of the next letter to type by 1

In the end, simply return False.

<details>
  
  ```python
   def can_word_be_typed(self, keyboard, word, jump_distance):
       if not word:
           return True
  
       letter_keyboard_positions_map = defaultdict(list)
       for r in range(len(keyboard)):
           for c in range(len(keyboard[0])):
               letter_keyboard_positions_map[keyboard[r][c]].append((r, c))
       
       queue = deque()
       for position in letter_keyboard_positions_map[word[0]]:
           queue.append(position)
  
       next_letter_idx = 1
       while queue:
           if next_letter_idx == len(word):
               return True 
  
           level_size = len(queue)
           for _ in range(level_size):         
               pos = queue.popleft()
               for next_position in letter_keyboard_positions_map[word[next_letter_idx]]:
                   if abs(next_position[0] - position[0]) + abs(next_position[1] - position[1]) <= jump_distance:
                       queue.append(next_position)
           next_letter_idx += 1
           
       return False
  ```
</details>


