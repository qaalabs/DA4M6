## **MORNING SESSION RUN SHEET - MLR**

**Day 2: 9:30-12:10**

---

## **9:30-9:40 (10 mins) - WELCOME**

**What you do:**

- Welcome back
- "Today: Multiple Linear Regression in morning, Time Series in afternoon"
- Check VMs loaded
- "Download the Day 2 zip file from [your short link]"
- "Extract to your VM"

**Files they need:**

- clocks.csv
- clocks_expanded_numeric.csv
- Clocks_Basic_MLR.R
- Clocks_Extended_Demo.R
- Clocks_Variables_README.txt
- gapminder.csv
- Gapminder_Task.txt

---

## **9:40-10:40 (60 mins) - SESSION 1: CLOCKS MLR**

### **9:40-9:45 (5 mins) - Introduction**

**What you say:**

- "Open Clocks_Basic_MLR.R"
- **Objective**: "By the end of this session, you'll be able to build and interpret an MLR model with multiple predictors"
- **Experience check** (Relay): "What did you learn about SLR yesterday?" (ask 2-3 people)
- **Application**: "How might using multiple variables help in your workplace?"

---

### **9:45-10:00 (15 mins) - Part 1: SLR to MLR**

**What you do:**

- Run through MODEL 1 (SLR review) together
- They follow along in their R script

**Questions to ask** (Overhead - just wait for volunteers):

- "What was the R-squared yesterday with just Age?" 
- [Run MODEL 2 - MLR]
- "Now look at the new R-squared. What changed?"
- "Why did it improve?"
- "Look at the p-values. Are both variables significant?"
- "Which variable has a bigger impact on price - Age or Bidders?"

**Key point:** Show them the comparison - 53% vs 89%

---

### **10:00-10:20 (20 mins) - Part 2: Adding More Variables**

**What you say:**

- "Now open clocks_expanded_numeric.csv and Clocks_Extended_Demo.R"
- "This has more information about each clock"
- "Open Clocks_Variables_README.txt to see what the numbers mean"

**What you do:**

- Run MODEL 1 (Age + Bidders) - they've seen this
- Run MODEL 2 (add Condition) together

**Questions to ask** (Overhead):

- "What happened to R-squared?"
- "Is Condition significant? How do you know?"
- Run MODEL 3 (add Style)
- "Better or worse?"
- Run MODEL 4 (add Material)
- "Which variables are significant now?"

**Keep moving through the models - don't get stuck**

---

### **10:20-10:35 (15 mins) - Part 3: Experimentation**

**What you say:**

- "Now you try different combinations"
- "Your task: find the best model"
- "Try removing non-significant variables"
- "Try different combinations"
- "Which gives the best R-squared?"

**What they do:**

- Work individually or pairs
- Experiment with the formulas
- You walk around (or pop into breakout rooms if online)

**Coach with questions:**

- "What have you tried?"
- "Which variables seem to matter?"
- "What happened when you removed that variable?"

---

### **10:35-10:40 (5 mins) - Quick Discussion**

**Questions** (Relay - ask multiple people):

- "What did you discover?"
- "Which variables mattered most?"
- "Did more variables always mean better R-squared?"

**Transition:** "You've now built MLR models with multiple variables. After break, you'll apply this to a new dataset."

---

## **10:40-11:00 (20 mins) - BREAK**

---

## **11:00-12:10 (70 mins) - SESSION 2: GAPMINDER TASK**

### **11:00-11:10 (10 mins) - Introduce Task**

**What you say:**

- "Open Gapminder_Task.txt"
- Read through the requirements together
- "You're predicting life_expectancy in Asia"
- "Use: age5_surviving, babies_per_woman, population, gdp_per_day"
- "Find which variables are significant"
- "Remove non-significant ones and rebuild"

**Setup breakout rooms:**

- "You'll work in pairs for 30 minutes"
- "One person shares screen, swap halfway"
- "I'll pop into rooms to help"
- Assign pairs / create breakout rooms

---

### **11:10-11:40 (30 mins) - Pairs Work**

**What they do:**

- Work in breakout rooms
- Build MLR models
- Experiment with variables

**What you do:**

- Visit each breakout room (5-7 mins per room)
  
**Coach with questions:**

- "How's it going?"
- "What have you tried?"
- "What's the error telling you?"
- "Which variables look significant?"

*Don't give answers - guide with questions*

---

### **11:40-11:55 (15 mins) - Solution Discussion**

**Bring everyone back to main room**

**What you say:**

- "Who wants to share their approach?" (Overhead - wait for volunteer)
- Get 2-3 learners to share their screens
- "What did you find? Which variables were significant?"
- "What R-squared did you get?"
- "Did anyone try different combinations?"

**Then show your approach:**

- Walk through one solution
- "Here's one way to do it..."
- Compare with what they found

**Keep it conversational - not a lecture**

---

### **11:55-12:05 (10 mins) - Recap with PPP Questions**

**Ask these questions** (PPP - name AFTER question):

- "What's the formula format for MLR in R?" [pause] "Sarah?"
- "How do we know if a variable is significant?" [pause] "Tom?"
- "What does R-squared tell us?" [pause] "Emma?"
- "Why might we remove a variable even if it increases R-squared slightly?" [pause] "David?"

**Make sure different people answer each question**

---

### **12:05-12:10 (5 mins) - Review**

**What you say:**

- "You've achieved today's objective - you can build and interpret MLR models"

**Learning transfer** (Relay - ask each person or 4-5 people):

- "Give me one specific example of how you'll use MLR in your work"
- Wait for answers from multiple people

**Bridge to afternoon:**

- "After lunch: Time Series analysis"
- "We'll look at data that changes over time"

---

## **12:10-13:20 (70 mins) - LUNCH**

---

## **YOUR PREPARATION CHECKLIST**

Tonight:

- [ ] Add all files to Day 2 zip
- [ ] Upload to Google Cloud
- [ ] Test short link works
- [ ] Print this run sheet
- [ ] Have it open on second screen tomorrow

Tomorrow morning:

- [ ] Test VM before 9:30
- [ ] Have run sheet visible
- [ ] Have files open ready to share screen
- [ ] Take a breath - you've got this!

---

**KEY REMINDERS:**

- Use Overhead questions (wait for volunteers)
- Use Relay for multiple answers
- Use PPP for checking (name after question)
- Coach don't tell in breakout rooms
- It's OK to say "good question, what do you think?"
- Silence is OK - count to 5 before helping

**You've got this! The structure is solid.**
