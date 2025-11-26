# HYPOTHESIS TESTING
*50 MINUTE SESSION RUN SHEET*

## **PREPARATION**

**Before session:**
- Pre-written scenarios ready (see below)
- Ticks & Crosses loaded with confidence poll
- Breakout rooms configured (pairs)
- Spurious correlations website queued: https://www.tylervigen.com/spurious-correlations
- Timer visible (only to you)

**Materials in chat:**
- Link to spurious correlations
- Scenario cards for breakout work

---

## **INTRODUCTION SECTION (5 mins) - 09:30-09:35**

### **Purpose (30 secs)**
"Welcome back. This session is called **Hypothesis Testing**."

### **Objective (30 secs)**
"By the end of this 50-minute session, you'll be able to formulate null and alternative hypotheses for a given scenario, and explain why statistics can reject the null hypothesis but cannot prove the alternative hypothesis, using real-world examples."

### **Process (1 min)**
"Here's how we'll structure the next 50 minutes:
- We'll start by investigating what hypotheses actually are using workplace scenarios
- You'll work in pairs to formulate your own hypotheses
- We'll discover together why statistics has some interesting limitations
- You'll practice interpreting different scenarios
- We'll recap the key points
- Then after this session, we'll see all of this in action when we walk through the Python and R code together

No slides today - this is all about building understanding through investigation and discussion."

### **Experience (1.5 mins)**
**[RELAY TECHNIQUE]**

"What's your experience with hypothesis testing? Have you encountered it before - maybe in your workplace, in previous study, or heard colleagues mention it?"

**[Go round 4-5 learners using Relay - starting with different person each time]**

Listen for:
- University statistics courses
- Workplace A/B testing
- Complete novices
- Those who've heard terms but don't understand

**[Adjust mental note of expertise level]**

### **Application (1.5 mins)**
**[OVERHEAD TECHNIQUE]**

"Thinking about your role as data analysts or data engineers - where might hypothesis testing be useful in your work?"

**[Wait for volunteer responses - take 2-3 answers]**

Likely answers:
- Testing if a change improved performance
- Seeing if two variables are related
- A/B testing features
- Checking if patterns are real or coincidence

"Exactly - and that last point about 'real or coincidence' is going to be crucial today. Let's dive in."

---

## **GUIDED LEARNING PART 1: WHAT ARE HYPOTHESES? (12 mins) - 09:35-09:47**

### **Setup the scenario (2 mins)**

"Imagine your boss comes to you and says: 'I want to know if there's a relationship between the number of people entering our store and the total sales amount.' 

What would you do as a data analyst?"

**[OVERHEAD - wait for responses]**

Expected: "Look at the data", "Check correlation", "Run some analysis"

"Right - but BEFORE we touch any code or data, statisticians do something clever. They formulate TWO competing statements. Let me show you."

**[Share screen or type in chat]:**

**Scenario:** Is there a relationship between number of people entering store and total sales?

**Statement 1:** "There is NO relationship between number of people entering store and total sales"

**Statement 2:** "There IS a relationship between number of people entering store and total sales"

"Notice something interesting about Statement 1? It's **negative** - it denies the relationship. We call this the **Null Hypothesis**, written as H₀."

"Statement 2 is the **Alternative Hypothesis**, written as H₁ or Hₐ."

### **Guided questions on structure (3 mins)**

**[OVERHEAD TECHNIQUE]**

"Looking at these two statements - what do you notice about how they relate to each other?"

**[Wait - accept various observations]**

"They're opposites of each other - exactly. One must be true, the other must be false. They can't both be true."

"Why do you think H₀ always sounds negative - always denying the relationship?"

**[OVERHEAD - wait]**

"Good question to park - we'll discover why in about 10 minutes when we see how the process works."

### **Individual practice - formulation (5 mins)**

"Let's practice formulating hypotheses. I'm going to give you a scenario, and I want EACH of you individually to type in the chat:
1. Your H₀ (null hypothesis)
2. Your H₁ (alternative hypothesis)"

**[Put in chat]:**

**Scenario:** Is there a relationship between the engine size of a vehicle and the amount of CO₂ emissions produced?

**Instructions:**
- Type your H₀ first
- Then type your H₁
- You have 2 minutes

**[Start timer - visible to you only]**

**[Monitor chat - watch for:]**
- Correct structure (H₀ denies, H₁ affirms)
- Common errors (swapping them, unclear wording)
- Who's not responding

**[After 2 mins]**

"OK, let's see what we've got."

**[Screen share 2-3 examples from chat - choose:]**
1. One perfect example
2. One with minor wording issue
3. One that swapped H₀ and H₁ (if any)

**[For each]:**
"This one from [name] - what's good about this? What could be clearer?"

**[Correct version]:**
- H₀: There is no relationship between engine size and CO₂ emissions
- H₁: There is a relationship between engine size and CO₂ emissions

### **Check understanding (2 mins)**

**[TICKS & CROSSES - quick poll]**

"Quick confidence check - how confident are you that you can now write H₀ and H₁ for a new scenario?

Green tick = confident
Red cross = need more practice"

**[Check results]**

**[If mostly green]:** "Excellent, let's move on."

**[If significant red crosses]:** "OK, let me give you one more quick example..."

**[Quick example if needed]:**
"Your manager asks: Does social media advertising increase website traffic?
- H₀: Social media advertising does NOT increase website traffic  
- H₁: Social media advertising DOES increase website traffic"

"Notice the pattern? H₀ always denies the relationship. Let's move on to discover WHY we structure it this way."

---

## **GUIDED LEARNING PART 2: THE INFINITY PROBLEM (15 mins) - 09:47-10:02**

### **Investigation setup (2 mins)**

"Now we're going to investigate something really interesting about statistics. I'm going to show you some data, and I want you to think carefully about what you can conclude from it."

**[Share screen or type in chat]:**

**Dataset:**
```
Variable 1:  1    2    3
Variable 2:  2    4    6
```

"Looking at this data - what do you notice?"

**[OVERHEAD - wait for responses]**

Expected: "Second one is double", "There's a pattern", "It's 2x"

"Right - Variable 2 seems to be double Variable 1."

### **The crucial question (3 mins)**

"Here's the key question, and I want you to think carefully before answering."

**[TICKS & CROSSES]**

"Is this pattern more likely to be:
- Green tick = a TRUE DEPENDENCY (Variable 2 is actually 2x Variable 1)
- Red cross = just a COINCIDENCE (happened by chance)"

**[Pause - let them vote]**

**[Check results]**

"Most of you said dependency - makes sense. But here's the critical follow-up question:"

**[OVERHEAD TECHNIQUE]**

"Can you **prove** it's a dependency from just these 3 data points?"

**[Wait for responses]**

Expected: "No", "Need more data", "Could be coincidence"

"Exactly - you can't prove it. So what would you want?"

Expected: "More data points"

"Right - let's give you more data."

### **Adding more data (4 mins)**

**[Update display]:**
```
Variable 1:  1    2    3    4    5    6
Variable 2:  2    4    6    8   10   12
```

"Now what do you think? More confident it's a dependency?"

**[OVERHEAD - quick responses]**

"OK, but here's the question I really want you to think about:"

**[Speak slowly and clearly]**

"Is there ANY CHANCE - no matter how small - that this is STILL just a coincidence?"

**[Pause - let silence sit]**

**[OVERHEAD - wait for answer]**

Expected: "Yes, there's a small chance"

"Right. Small chance, but non-zero. Now imagine we have 100 data points, same pattern. Still a chance it's coincidence?"

**[Wait]**

"Yes - tiny, but still non-zero. What about 1,000 data points? 1 million?"

### **The key insight - breakout rooms (5 mins)**

"I'm going to put you in pairs for 3 minutes to discuss this question:"

**[Put in chat]:**

**Discuss in your pair:**
How many data points would you need for the chance of it being a coincidence to go down to EXACTLY zero?

Think about this carefully - we're not talking about 'good enough for practical purposes' - we're asking when does the probability reach exactly 0?

**You have 3 minutes - go.**

**[Launch breakout rooms - pairs]**

**[Visit 2-3 rooms to listen]**

**[After 3 mins - bring back]**

### **Discovery moment (1 min)**

**[PPP TECHNIQUE]**

"So - how many data points do you need for the probability to be exactly zero? What did you conclude in your pairs?"

**[Pose, pause, then pick someone]**

"[Name]?"

Expected answers:
- "Infinite"
- "You never get to zero"
- "It's always non-zero"

"Exactly. Formally, you'd need INFINITE data points. And since we can never have infinite data points..."

**[Let them complete the thought]**

"...there will ALWAYS be a chance - no matter how small - that it's just a coincidence."

**[Pause - let this land]**

"This is why statistics can NEVER **prove** the presence of a dependency. Because there's always that tiny, tiny chance it's all just coincidence."

"From a practical perspective, we reach a cut-off point where we're happy to accept it as a rule. But theoretically - we've never proven it."

---

## **GUIDED LEARNING PART 3: THE OTHER EXTREME (10 mins) - 10:02-10:12**

### **Second scenario (2 mins)**

"Now let's look at the opposite extreme."

**[Share screen or type in chat]:**

```
Variable 1:  1      2      3        4      5
Variable 2: 25   -240   3400      0     -1
```

**[OVERHEAD TECHNIQUE]**

"Can you spot a dependency here?"

**[Wait for responses]**

Expected: "No", "Looks random", "Can't see a pattern"

"Right - looks like there's no dependency. But here's the question:"

### **The second infinity problem (3 mins)**

"Can you **prove** there's NO dependency?"

**[Pause]**

**[OVERHEAD]**

"What could you do to try?"

Expected: "Try different models", "Look for patterns", "Run different tests"

"Right - you could try another model. And another. And another. You try every model you know - and still don't find a dependency."

"Does that prove there's no dependency?"

**[TICKS & CROSSES]**

"Green tick = Yes, if I tried all known models and found nothing, I've proven no dependency
Red cross = No, I still haven't proven no dependency"

**[Check results]**

### **The key insight (2 mins)**

"Those of you who said red cross - you're right. Why?"

**[OVERHEAD - wait]**

Expected: "There might be a model we don't know yet", "Could be a pattern we can't detect"

"Exactly. There could be another model - not discovered yet - that explains this sequence perfectly."

"So we can NEVER prove the ABSENCE of a dependency, because there might be a dependency that our models simply couldn't find."

### **Summary of both extremes (3 mins)**

**[Type in chat or speak clearly]:**

"So statistics balances between two extreme cases:

1. **Cannot prove PRESENCE of dependency** - it might just be a coincidence (no matter how many data points we have)

2. **Cannot prove ABSENCE of dependency** - there might be a dependency our models can't detect

The ONLY thing statistics can do is **reject the claim that there's NO dependency** - in other words, reject H₀."

**[Pause - let this sink in]**

"And THIS is why we always start with H₀ - the null hypothesis that denies the relationship. Because the only thing we can actually do is try to disprove it."

"If we gather enough evidence to reject H₀ with high confidence, we MIGHT then decide to ACCEPT H₁. But we never prove H₁."

---

## **GUIDED LEARNING PART 4: REAL-WORLD EXAMPLE (8 mins) - 10:12-10:20**

### **Setup the example (1 min)**

"Let me give you a real-world example that brings this together."

**[OVERHEAD TECHNIQUE]**

"Do you believe that smoking causes cancer? Not asking for scientific proof - just your personal belief.

Green tick = Yes, I believe smoking causes cancer
Red cross = No, I don't believe it"

**[Ticks & Crosses poll]**

**[Check results - likely mostly green]**

### **The evidence (2 mins)**

"Most of you believe it - makes sense. Scientists have been researching this for over 50 years, with massive datasets."

"But here's something interesting: they've never been able to get a correlation coefficient higher than 0.65. That's moderate - not even strong."

"Now let me show you something else."

### **Spurious correlations investigation (4 mins)**

**[Share screen - go to tylervigen.com/spurious-correlations]**

"This website collects spurious correlations - patterns in data that are almost certainly just coincidence."

**[Show the cheese/bedsheet example or similar with correlation ~0.95]**

"Look at this - correlation of 0.95. Much higher than the smoking/cancer correlation of 0.65."

**[Let silence sit for moment]**

**[OVERHEAD TECHNIQUE]**

"So how can you believe that smoking causes cancer (correlation 0.65) but dismiss this cheese example (correlation 0.95)?"

**[Wait for responses]**

Expected:
- "Cheese/bedsheet is obviously coincidence"
- "Smoking has more data behind it"
- "Makes logical sense vs doesn't"

### **The key distinction (1 min)**

"Exactly - and here's the key point. In BOTH cases:
- Scientists REJECTED H₀ (proved there IS a mathematical correlation)
- But they never PROVED H₁ (that one causes the other)

With smoking/cancer, we have 50+ years of data, billions of data points, and it makes biological sense - so we ACCEPT H₁ with high confidence.

With cheese/bedsheets, we recognize it's probably just coincidence despite the high correlation.

The decision to ACCEPT H₁ is based on:
- Size of dataset
- Biological/logical plausibility  
- Subject knowledge
- Context

But we never actually prove it."

---

## **CONSOLIDATION - STRUCTURED RECAP (8 mins) - 10:20-10:28**

### **Key concepts check (5 mins)**

"Let's recap the key points. I'm going to ask some checking questions."

**[PPP TECHNIQUE throughout this section]**

**Question 1:**
"What are the two hypotheses we always formulate when doing hypothesis testing?"

**[Pose, pause, person - pick someone who hasn't spoken much]**

Expected: "Null hypothesis and alternative hypothesis" or "H₀ and H₁"

"Good - and which one always denies the relationship?"

**[Quick follow-up to same person or another]**

Expected: "H₀ - the null hypothesis"

---

**Question 2:**
"Why can statistics never prove the presence of a dependency?"

**[Pose, pause, person - pick different learner]**

Expected: "Because there's always a chance it's just coincidence, no matter how much data we have"

"Exactly - we'd need infinite data points for that chance to be exactly zero."

---

**Question 3:**
"Why can statistics never prove the absence of a dependency?"

**[Pose, pause, person]**

Expected: "Because there might be a model we haven't found yet that would show a dependency"

"Right - there could be a dependency our current models simply can't detect."

---

**Question 4:**
"So what's the ONLY thing statistics can actually do?"

**[Pose, pause, person]**

Expected: "Reject H₀" or "Disprove the null hypothesis"

"Exactly. We can gather evidence to reject H₀. If we do that with high confidence, we might decide to accept H₁ - but we never prove H₁."

---

### **Individual practice scenario (3 mins)**

"Final practice before we move to code. I want each of you individually to type in chat your answers to this scenario:"

**[Put in chat]:**

**Scenario:** 
You run a hypothesis test and get a correlation coefficient of 0.08 (very weak).

Type your answers:
1. Can you reject H₀?
2. Can you prove H₀?
3. Can you accept H₁?

**You have 90 seconds.**

**[Monitor chat]**

**[After 90 seconds]**

"Let's check. The answers are:
1. **No** - correlation is too weak, not enough evidence to reject H₀
2. **No** - we can never prove H₀ (that's not how it works)
3. **No** - because we haven't rejected H₀, so we have no basis to accept H₁

What's the outcome of this analysis? NOTHING. We couldn't gather enough evidence to reject H₀, so we can't accept H₁ either."

**[Screen share a few correct answers from chat to celebrate]**

---

## **REVIEW SECTION (2 mins) - 10:28-10:30**

### **Review of objective (30 secs)**

"Let's come back to our objective. We said by the end of 50 minutes, you'd be able to formulate H₀ and H₁ for a scenario, and explain why statistics can reject but not prove."

**[TICKS & CROSSES - confidence check]**

"How confident are you now that you could do this?

Green tick = Confident
Red cross = Still unsure"

**[Check results]**

**[If mostly green - celebrate]**
"Excellent - you've built the conceptual foundation."

**[If significant red crosses - briefly address]**
"OK - what specifically are you unsure about? Type in chat quickly."

**[Address 1-2 concerns if time allows]**

### **Bridge to code (1 min)**

"So now you understand:
- How to formulate H₀ and H₁
- Why we can only reject, never prove
- What it means when correlation is weak vs strong

In the next session, we're going to see all of this in action. When you see code that calculates p-values and correlation coefficients, you'll understand what those numbers actually mean."

"When the code asks you 'do we have enough evidence to reject H₀?' - you'll know exactly what that question means."

### **Next steps (30 secs)**

"The pattern you'll see in code is:
1. Formulate H₀ and H₁
2. Run the statistical test
3. Look at the evidence (correlation coefficient, p-value)
4. Decide: can we reject H₀?
5. If yes, do we have enough confidence to accept H₁?

You've got the logic - now let's see it in practice."

---

## **TIMING CHECK**

Total: 50 mins
- Introduction: 5 mins
- Part 1 (Hypotheses): 12 mins  
- Part 2 (Infinity problem): 15 mins
- Part 3 (Other extreme): 10 mins
- Part 4 (Real-world): 8 mins
- Consolidation: 8 mins
- Review: 2 mins

---

## **KEY FACILITATION NOTES**

**Question techniques used:**
- **Relay:** Experience check (introduction)
- **Overhead:** Throughout guided learning for open discovery
- **PPP:** Consolidation section for individual checking

**Individual accountability:**
- Chat responses for H₀/H₁ formulation (twice)
- Ticks & Crosses confidence checks (3 times)
- PPP questions in recap (all learners)

**Breakout rooms:**
- One structured discussion (infinity problem)
- Clear question and time limit
- Specific output expected

**Traffic light moments:**
- After first H₀/H₁ practice
- Before moving to code walkthrough

**No slides, no bullets - all conversational discovery with strategic checkpoints.**

---

Would you like me to:
1. Adjust any timings?
2. Add more individual checkpoints?
3. Create backup questions for different ability levels?
4. Write suggested responses for common misconceptions?
