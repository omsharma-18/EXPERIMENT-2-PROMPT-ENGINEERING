# EXP-2-PROMPT-ENGINEERING-

## Aim: 
Comparative Analysis of different types of Prompting patterns and explain with Various Test Scenarios

## Experiment:
We designed an experiment to evaluate the effectiveness of prompting strategies.

1. **Prompt Types:**

   * **Unstructured / Broad Prompts**: Vague and open-ended.
   * **Structured / Refined Prompts**: Clear, concise, and directive.

2. **Evaluation Metrics:**

   * **Quality** – Relevance and usefulness of the output.
   * **Accuracy** – Correctness of facts, consistency with input.
   * **Depth** – Level of detail and explanation.

3. **Scenarios Tested:**

   * General Knowledge (e.g., history, science)
   * Creative Writing (e.g., storytelling, poem)
   * Problem Solving (e.g., coding, logic puzzles)
   * Instruction Following (e.g., step-by-step tasks)
   * Analytical Reasoning (e.g., pros & cons, comparative answers)



## Algorithm:

1. Select a **set of prompts** for each scenario.
2. Run the prompts through the AI model with **two variations**:

   * Broad/unstructured form.
   * Refined/structured form.
3. Collect responses for both types.
4. Analyze and compare responses against the evaluation metrics.
5. Record observations and summarize insights.

## Test Scenarios & Results

### **1. Zero-Shot Prompting**

**Definition:** Asking the model to perform a task without giving any examples.
**When to use:** General tasks where the model already has good knowledge.

* **Strengths:** Fast, minimal input, tests model’s generalization.
* **Weaknesses:** May be vague, inconsistent for complex tasks.

**Test Scenario:**
 Task: *Summarize the following passage in 2 lines.*

* **Prompt:**
  “Summarize the following passage in 2 lines:
  ‘Artificial Intelligence is transforming industries by automating repetitive tasks, improving decision-making, and enabling new innovations in healthcare, finance, and education.’”

* **Output:**
  “AI automates tasks, enhances decision-making, and drives innovation across industries like healthcare, finance, and education.”

 Works well because it’s straightforward.

---

### **2. One-Shot Prompting**

**Definition:** Asking the model with **one example** of the desired input-output format.
**When to use:** Slightly complex tasks that need clarity.

* **Strengths:** Reduces ambiguity, better consistency.
* **Weaknesses:** Limited generalization if example is biased.

**Test Scenario:**
 Task: *Convert sentences into passive voice.*

* **Prompt:**
  “Example:
  Active: The chef cooked the meal.
  Passive: The meal was cooked by the chef.

Now, convert this:
Active: The teacher explained the lesson.”

* **Output:**
  “Passive: The lesson was explained by the teacher.”

 Example clarified the expected transformation.

---

### **3. Few-Shot Prompting**

**Definition:** Providing **multiple examples** before asking the model to perform the task.
**When to use:** Complex tasks requiring demonstration of patterns.

* **Strengths:** High accuracy, shows context and format.
* **Weaknesses:** Longer prompts, may bias model to provided examples.

**Test Scenario:**
 Task: *Classify movie reviews as Positive or Negative.*

* **Prompt:**
  “Review: The movie was amazing, I loved every moment! → Positive
  Review: It was a waste of time, very boring. → Negative
  Review: The acting was incredible but the story felt weak. → Mixed
  Review: The film had stunning visuals but a weak script. → ?”

* **Output:**
  “Mixed”

 Few-shot examples teach the classification style.

---

### **4. Chain-of-Thought Prompting (CoT)**

**Definition:** Asking the model to **reason step by step**.
**When to use:** Logic-heavy, reasoning, or math-based problems.

* **Strengths:** Boosts reasoning, transparency of steps.
* **Weaknesses:** Longer outputs, sometimes over-explains.

**Test Scenario:**
 Task: *Solve a math problem.*

* **Prompt:**
  “Q: If a train travels 60 km in 1.5 hours, what is its speed in km/h? Think step by step.”

* **Output:**
  “Step 1: Distance = 60 km
  Step 2: Time = 1.5 hours
  Step 3: Speed = Distance / Time = 60 / 1.5 = 40 km/h
  Answer: 40 km/h”

 Explains reasoning, not just answer.

---

### **5. Self-Consistency Prompting**

**Definition:** Generate multiple reasoning paths and select the most consistent answer.
**When to use:** Complex reasoning tasks with multiple possible paths.

* **Strengths:** More reliable than single CoT.
* **Weaknesses:** Slower, requires multiple generations.

**Test Scenario:**
 Task: *Which is heavier: 1 kg of iron or 1 kg of cotton?*

* **Prompt (model internally tries multiple reasoning paths):**
  Path A: Iron is denser, but weight is same.
  Path B: Cotton looks larger, but weight is same.

* **Final Answer:**
  “Both weigh the same: 1 kg.”

 Eliminates wrong reasoning by checking consistency.

---

### **6. Instruction Prompting**

**Definition:** Giving **clear task-specific instructions** in imperative form.
**When to use:** Formal or structured outputs.

* **Strengths:** Precise, task-oriented, reliable.
* **Weaknesses:** Too rigid, may stifle creativity.

**Test Scenario:**
 Task: *Write a professional email requesting meeting reschedule.*

* **Prompt:**
  “Write a polite professional email asking your manager to reschedule tomorrow’s meeting to Friday afternoon.”

* **Output:**
  “Subject: Request to Reschedule Meeting
  Dear \[Manager],
  I hope this message finds you well. I would like to request rescheduling tomorrow’s meeting to Friday afternoon, if convenient for you. Thank you for your understanding.
  Best regards,
  \[Your Name]”

 Structured and professional.

---

### **7. Role Prompting**

**Definition:** Assigning the model a **specific role/persona** to influence its responses.
**When to use:** Simulations, interviews, creative storytelling.

* **Strengths:** Context-rich, more human-like responses.
* **Weaknesses:** May introduce bias from the role.

**Test Scenario:**
 Task: *Explain blockchain to a 10-year-old.*

* **Prompt:**
  “You are a friendly teacher. Explain blockchain to a 10-year-old using simple language.”

* **Output:**
  “Imagine a notebook that everyone shares. Whenever someone writes in it, everyone sees it and agrees it’s true. That’s how blockchain works—it’s a shared notebook that no one can cheat.”

 Persona improves tone and clarity.

---

## **Comparative Summary Table**

| Prompting Type   | Best For            | Pros                  | Cons                   | Example Task             |
| ---------------- | ------------------- | --------------------- | ---------------------- | ------------------------ |
| Zero-Shot        | Simple tasks        | Fast, minimal         | May be vague           | Summarization            |
| One-Shot         | Format-based tasks  | Reduces ambiguity     | Limited generalization | Passive voice conversion |
| Few-Shot         | Complex tasks       | High accuracy         | Long prompts           | Sentiment classification |
| CoT              | Reasoning/math      | Transparent reasoning | Verbose                | Math problems            |
| Self-Consistency | Ambiguous reasoning | Reliable              | Slow                   | Trick questions          |
| Instruction      | Structured tasks    | Precise               | Less creative          | Email writing            |
| Role Prompting   | Creative/explaining | Natural, engaging     | Biased responses       | Teaching kids            |

---

## Output
[Comparative_Analysis_of_Prompting_Patterns.pdf](https://github.com/user-attachments/files/22016769/Comparative_Analysis_of_Prompting_Patterns.pdf)

## Result
Broad prompts are useful for open-ended exploration but often lack precision.
Refined prompts consistently improve the quality, accuracy, and depth of responses.
The experiment demonstrates that prompt engineering is crucial for optimizing AI output across tasks.
