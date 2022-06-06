# Reading Assignment 36

## DSA Review

---

### Whiteboard Advice

- According to the Author, the best piece of advice when doing a whiteboard interview is to Communicate. This is split into six parts;
  - Restate the Question.
    - By doing this, you both verify you have a correct understanding of the problem and prove you can articulate a problem.
  - Ask about Edge Cases.
    - By doing this, you show you are analytical and will actively try and work towards preventing bugs.
  - Ask about Test Cases.
    - In some cases it is a necessary/expected question, but even if it isn't it shows that you are familiar enough with testing to ask about/think about it.
  - Write out pseudocode and verify it makes sense.
    - This way you can free yourself from language specific names and work towards the idea of what you are doing and shows your though process. As a bonus, you can also ask the interviewer if the pseudocode makes sense and they might provide some constructive feedback that you can use.
  - Write the actual code and verify it makes sense.
    - By asking if your solution looks good it shows you are articulate and easier to work with because you are willing to discuss ways to improve your work.
  - If stuck, don't be afraid to ask for help.
    - It isn't forbidden to ask for help if you are truly stuck, but it is best to phrase it conversationally.

---

### 7 Tips to Ace a Programming Interview

- According to the Author the following 7 tips are the ones that can help you ace the programming interview;
  - Take a few minutes
    - Once you have had the problem explained to you and clarifying questions have been asked, verbalize that you would like a few minutes to think over the problem and then afterwards re-engage, explain your conclusion and your reasoning.
  - Write down the steps
    - Write out the general very high-level steps to how you plan to solve it.
  - Write out the pseudocode first
    - Write out a basic version that is code agnostic and doesn't worry about simple issues, just the base logic being correct.
  - Don't sweat the small stuff
    - If you can't remember something simple like a language specific implementation of something, verbalize it and explain what you would put in the place of the pseudocode if you had access to google to look up what the language called it. Focus far more on the big picture than any of the small stuff.
  - Sit down and be humble
    - If given advice or criticism, make sure to take it well and use it. Take it as them thinking you are worth the effort and are extending an opportunity to demonstrate how you take feedback.
  - Come prepared
    - There is not substitute for time spent preparing for the interview. The more you prepare the more confident you will be in the interview and the smoother things will go.
  - Review your work
    - There won't always be time to finish questions, but in the occoisions where you have some time, make sure to spend it reviewing what you wrote down to catch any small mistakes. In particular, if you have the time, consider two things;
      - The Algorithmic Efficiency. For example, if it involves any kind of sorted dataset, there is likely a log(n) solution. And the amount of times that the solution involves a hashtable and thus O(1) lookup time with it is absurd. If you are looking for a better algorithm, try a hashtable.
      - Correctness. Have you accounted for edge cases? Such as an empty array, a negative number, of a string with a weird pattern. Maybe you won't find all of them, but it is far better to try finding them than to not try finding them and declare the solution finished.
