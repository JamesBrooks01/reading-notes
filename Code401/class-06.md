# Reading Assignment 06

## Ten Thousand Game 1

---

### How to use Random Module

---

- The random module in Python can provide functions that help with many different types of oeprations, but one of the most important is the ability to generate a random number.
- Some of the helpful function in the Random module are;
  - `Randint` for random integers with the two parameters defining the lower and upper limit of the range to generate.
  - `Random` a larger number gained by multiplying the `.random()` function by the upper limit.
  - `Choice` for a random value from the sequence provided.
  - `Shuffle` for shuffling elements in a list. This operation is done in place.
  - `Randrange` for a random element based on three parameters, Start, Stop and Step.

### What is Risk Analysis

---

- The probability of an unwanted incident is defined as a "Risk" and in Software Testing, risk analysis is the process of identifying the risks in applications or software you build and prioritizing tests to run after which the process of assigning the level of risk is done.
- But the first question to be asked is Why? Why use risk analysis?.
  - It highlights potential problem areas and if you know the risk areas you can actively mitigate risks, sometimes with a test plan where the risks involved in testing the product are taken into consideration alongside the possibility of any damage they could cause to the software and what the soloutions are.
- As for a short list of some potentiol risks that could be encountered;
  - New Hardware
  - New Technology
  - New Automations Tools
  - The Sequence of the Code
  - The Availability of Test Resources for the App
- There are also some unavoidable tests;
  - Time allocated to Testing
  - A defect leakage due to complexity or size of the application
  - Urgency from Clients to complete the project
  - Incomplete Requirements
- The are some areas where by approaching the situation carefully can help;
  - Conducting a risk assessment review meeting
  - Directing maximum effort to high-risk areas
  - Creating a risk assessment database for future use
  - Identify the risk magnitude indicators
- The risk magnitude indicators are as follows;
  - `High` where the effect would be very high and non-tolerable where the company would potentially face loss.
  - `Medium` where the effect would be tolerable but undesireable where the company would suffere finacially but has limited risk.
  - `Low` where the effect is tolerable and there is little external exposure or no financial loss.
- When identifying risks, it is important to know the different types of risks;
  - `Business Risks` are the most common and comes from the company or customer.
  - `Testing Risks` where you should be well aquainted with the platfomr and the software testing tools you are using.
  - `Premature Release Risk` where you should have a fair amount of knowledge of the risk assosiate with releasing an untested or unsatisfactory software.
  - `Software Risk` where you should be well-versed in the general risks of the software development process.+
- In the Risk Assessment Process the most important steps are;
  - First to assess the the three perspectives of Risk Assessment
    - Effect where you identify the conditon, event or action and determine it's impact.
    - Cause where you scan the problem and identify the reason behind it.
    - Likelihood where you aknowledge the possibility a requirement won't be satisfied.
  - Next, you perfore the actual Risk Analysis by;
    - Searching the Risk
    - Analyizing the impact of each Risk
    - Measureing each Risk

### Test Coverage

---

- As noted by the author, while trying to reach a target goal for test coverage might look good on paper, it misses the point of thouroghly testing the code.
- And if you make a certain level of coverage a goal, people will attempt to attain it which is easy to do if you sacrifice the quality of the tests.
- Often this distacts you with testing things that rarely go wrong from the things that really matter.
- Like most areas of programming, good testing requires thought and a while TDD is useful it doesn't always make for good test.
- The author believes that good, thoughful tests once done will have a coverage number in the upper 80s to 90s and any code that claims 100% coverage is likely someone writing test to make the numbers happy.
- The author says that testing is sufficient when you rarely get bugs that escape into production and you are hesitent to change code for the fear it will cause production bugs.
- A way to detrmine you are trying to test too much is when the test slow you down. Where a simple code change causes lengthy changes to tests.

### Big O Notation

---

- Big O is a programming way to describe the run-time of an algorithm.
- Some examples of Big O are;
  - O(1) where it executes in the same run-time regardless of it's input
  - O(n) where the run-time increases linearly with the input
  - O(n^2) where the run-time increases at a squared rate with the input.
- The four basic rules of Big O are;
  - The get the Big O, you add up the different steps
  - Drop the constants
  - For clarity use different variables for different inputs
  - Don't use non-dominent terms.
