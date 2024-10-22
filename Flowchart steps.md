# Flowchart Breakdown

## Main Flowchart:
### Start (Oval)
- Start of the program.

### Input (Parallelogram)
- "Input: number of rounds" (Prompt the player for how many rounds they want to play).

### Input (Parallelogram)
- "Input: difficulty level" (Player selects difficulty: 1-10, 1-50, or 1-1000).

### Action (Rectangle)
- "Set `max_number` based on difficulty" (Set the guessing range based on the difficulty chosen by the player).

### Action (Rectangle)
- "Initialize `total_attempts` to 0" (Total attempts will store the sum of all attempts made across rounds).

### Action (Rectangle)
- "Loop through each round" (Repeat the process for the number of rounds defined by the player).

### For Each Round:
#### Action (Rectangle)
- "Generate a random number between 1 and `max_number`" (Randomly select a number based on the difficulty).

#### Recursive Call: Guess Number
- Call the `guess_number` function to manage the guessing process. This function handles all attempts for the current round.

#### Action (Rectangle)
- "Add number of attempts to `total_attempts`" (Update the total number of attempts after each round).

### Decision (Diamond)
- "Are all rounds complete?" (Check if all rounds have been played).

### If Yes:
- Proceed to calculate the average attempts.

### If No:
- Loop back to start a new round.

### Action (Rectangle)
- "Calculate average attempts per round" (Divide `total_attempts` by the number of rounds).

### Output (Parallelogram)
- "Display average number of attempts" (Print the average number of attempts after the game ends).

### End (Oval)
- End of the program.

---

## Sub-Flowchart: Guess Number (Recursive Function)
### Start (Oval)
- Start of the `guess_number` function.

### Action (Rectangle)
- "Start timing for player response" (Use `time.time()` to record the starting time).

### Input (Parallelogram)
- "Input: user guess" (Prompt the player to enter their guess).

### Action (Rectangle)
- "Stop timing and calculate response time" (Calculate the total time taken for the player to respond).

### Output (Parallelogram)
- "Display response time" (Show the player how long they took to respond).

### Decision (Diamond)
- "Is guess equal to the random number?" (Check if the player's guess matches the random number).

### If Yes:
- **Output (Parallelogram)**: "Print correct guess and number of attempts" (Display a success message with the number of attempts taken for the round).
- **Return**: Exit the recursive function and return the number of attempts.

### If No:
#### Decision (Diamond): "Is guess too high?"
- **If Yes**:
  - **Output (Parallelogram)**: "Print 'Too High'"
  
- **If No**:
  - **Output (Parallelogram)**: "Print 'Too Low'"

### Recursive Action (Rectangle)
- "Recursively call `guess_number`" (Repeat the process until the player guesses correctly).

### End (Oval)
- End of the function (When the correct guess is made).

---

## Flowchart Summary:
1. **Main flowchart** for managing rounds and difficulty.
2. **Sub-flowchart** for the guessing logic that recursively handles player guesses, feedback, and response time measurement.
