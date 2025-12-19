# Assignment 6: Prompt Engineering for Performance Improvement

**Task Selected:** Structured Data Extraction (from unstructured text reviews into JSON format)  
**LLM Used:** Hugging Face Transformers (OpenAI API optional)

---

## 📌 Baseline Prompt
- **Prompt:** `"Extract the data."`  
- **Goal:** Extract fields (Name, Price, Date) from a text review.  
- **Observation:** Output was unstructured and inaccurate.  
- **Accuracy Score:** 2/10  

---

## 🔑 Prompt Engineering Techniques

### 1. Role Prompting
- **Prompt:** `"Act as a Senior Data Analyst. Extract Name, Price, Date from the review."`  
- **Observation:** Better extraction, but still unstructured.  
- **Accuracy Score:** 5/10  

### 2. Output Formatting
- **Prompt:** `"Provide the output in JSON format with keys: Name, Price, Date."`  
- **Observation:** JSON-like output produced, but formatting errors.  
- **Accuracy Score:** 7/10  

### 3. Chain-of-Thought (CoT)
- **Prompt:** `"Before providing the final answer, list the steps you will take to reach the solution. Then give the JSON output."`  
- **Observation:** Reasoning steps improved accuracy and structure.  
- **Accuracy Score:** 8/10  

### 4. Final Optimized Prompt
- **Prompt:**  `"Act as a Senior Data Analyst. First explain your reasoning briefly. Then provide the output in strict JSON format with keys: Name, Price, Date."`
- **Observation:** Combined techniques produced structured, accurate JSON.  
- **Accuracy Score:** 9/10  

---

## 📊 Results Summary

| Prompt Type        | Example Prompt | Accuracy Score (1–10) | Observation |
|--------------------|----------------|------------------------|-------------|
| Baseline           | "Extract the data." | 2 | Poor, unstructured |
| Role Prompting     | "Act as a Senior Data Analyst..." | 5 | Better extraction |
| Output Formatting  | "Provide JSON output..." | 7 | Structured but imperfect |
| Chain-of-Thought   | "List steps then JSON..." | 8 | Reasoning improves accuracy |
| Final Optimized    | Combined techniques | 9 | Best result |

---

## 📘 Key Lessons Learned
- Prompt engineering **directly impacts LLM performance**.  
- **Role prompting** improves contextual accuracy.  
- **Output formatting** ensures structured results.  
- **Chain-of-thought reasoning** enhances reliability.  
- Combining techniques yields the **highest-quality outputs**.  

---

## ⚙️ Environment Setup
- **Tools:** Anaconda Navigator, JupyterLab  
- **Packages:**  
```bash
conda install -c conda-forge transformers
conda install -c conda-forge torch

*Livan Hagi Osman*
