# The Ultimate Guide to Cracking Coding Interview Problems

Many candidates fail not because they don't know the code, but because they jump into coding too fast. This guide outlines the **REACTO** method—a structured approach to solving any problem in an interview setting.

---

## 1. R - Repeat & Rephrase
**Never start coding immediately.**
- **Listen carefully** to the problem statement.
- **Repeat the problem** back to the interviewer in your own words to ensure you understood it.
- **Ask clarifying questions**:
    - "Can the array contain negative numbers?"
    - "What should I return if the input is empty?"
    - "Is the list sorted?" (This is a huge hint! If sorted, think Binary Search or Two Pointers).

## 2. E - Examples (Test Cases)
Before thinking about the logistics, write down input/output pairs.
- **Happy Path**: Standard simple input. `Input: [1, 2, 3], Output: 6`
- **Edge Cases**: Empty input, single element, negative numbers, very large numbers.
- *Tip*: This buys you thinking time and shows you are detail-oriented.

## 3. A - Approach (The "How")
Talk through your strategy *out loud*.
- **Brute Force First**: "I could simpler iterate through every pair..." (High Time Complexity). It's okay to start here!
- **Optimize**: "But we can do better by using a Hash Map to store visited numbers..."
- **Discuss Trade-offs**: Discuss Time Complexity (Big O) and Space Complexity.
- **Get Buy-in**: Ask the interviewer, "Does this approach sound good to you?" before writing a single line of code.

## 4. C - Code
Now, and only now, write the code.
- **Write clean code**: Use descriptive variable names (`currentIndex` vs `i`, `maxProfit` vs `p`).
- **Modularize**: If a part of the logic is complex, helper functions are your friend. `if (isValid(node)) { ... }`
- **Speak while you type**: "I'm initializing the accumulator here...", "Now I'm iterating through the list..."

## 5. T - Test (Dry Run)
Don't wait for the interviewer to find bugs.
- **Walk through your code** line-by-line with one of your examples from step 2.
- Update variable values manually on the side (trace table).
- Catch off-by-one errors here.

## 6. O - Optimize (Refactor)
- Look for redundant code.
- Can you make it cleaner?
- Double-check: Did you handle all edge cases?

---

## Common Patterns to Master
(We will cover these in Month 2)
1. **Two Pointers**: Moving from ends to middle (or sticking to a window).
2. **Sliding Window**: Sub-arrays & substrings.
3. **Hash Maps**: Instant lookups (Frequency counting).
4. **Binary Search**: Sorted data.
5. **Recursion/DFS/BFS**: Trees and Graphs.

## Mindset Tips
- **Stuck?** State what you know. "I know I need to track the global maximum, but I'm struggling with the update condition." The interviewer is a co-worker, not an examiner; they will often drop a hint.
- **Silence is bad**: Keep the monologue going.
- **Be teachable**: If they suggest a change, listen and adapt.
