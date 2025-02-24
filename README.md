# Idiomatic Bridges: A Cross-Linguistic English-Spanish Idiom Alignment Dataset

📌 **Version:** 1.0  
📌 **Authors:** Belén Saavedra, Nagore Bravo, Juliana Planas  
📌 **Base Resource:** [IdioTS Dataset](https://huggingface.co/datasets/fdelucaf/IdioTS)  

---

## 📖 About the Project  
**Idiomatic Bridges** is a bilingual **English-Spanish idiom alignment dataset** designed to improve **machine translation, NLP applications, and linguistic studies**. This dataset extends and refines the **IdioTS dataset**, incorporating **new idioms, revised translations, and expanded annotations** to enhance cross-linguistic idiomatic analysis.

---

## 📂 Dataset Overview  
The dataset contains **125 English idioms** annotated with **Spanish equivalents**, along with semantic and syntactic similarity ratings. It includes:  

✅ **English idiom** (original)  
✅ **Spanish equivalent** (best matching translation)  
✅ **Example sentences** in both languages  
✅ **Semantic similarity (1-3 scale)**  
✅ **Syntactic similarity (1-3 scale)**  
✅ **Annotation notes** (explanations for difficult cases)  

### **Data Format**  
The dataset is available in **TSV** format for compatibility with various NLP tools.  

| Idiom_EN         | Idiom_ES         | Example_EN                          | Example_ES                          | Semantic_Similarity | Syntactic_Similarity | Notes |
|-----------------|-----------------|-------------------------------------|-------------------------------------|----------------------|----------------------|-------|
| to ring a bell    | me suena     | The name rings a bell | Su nombre me suena | 3 | 3 |  |
| under the weather | estar pachucho | Jared won’t be coming in today because he’s feeling under the weather. | Jared no va a venir hoy porque está pachucho. | 2 | 3 | Significant cultural difference |

---

## 🛠️ Methodology  
The dataset was constructed following a structured annotation process:  

1. **Selection of Idioms:** The IdioTS dataset was used as a base, but additional idioms were identified, and some existing translations were modified.  
2. **Annotation Process:**
   - **Step 1:** All three annotators **independently annotated 25 idioms** to establish a baseline for **Inter-Annotator Agreement (IAA)**.  
   - **Step 2:** The remaining 120 idioms were **split equally (40 each)** among annotators.  
3. **Annotation Guidelines:**
   - Identifying the **best idiomatic match** in Spanish.  
   - Rating **semantic similarity (1-3)** and **syntactic similarity (1-3)**.  
   - Providing **example sentences** and **notes on translation challenges**.  

---

## 📊 Inter-Annotator Agreement (IAA)  
To measure annotation consistency, we computed the following metrics using **R**:

- **Observed Agreement** (simple percentage of matching labels).  
- **Fleiss’ Kappa** (for agreement among three annotators).  
- **Cohen’s Kappa** (for pairwise comparisons).  

**Results:**  
Initial nominal agreement measures indicated low consistency among annotators, with observed agreement at 25% for semantic and 35% for syntactic dimensions, and Fleiss' kappa values (0.134 and 0.205, respectively) suggesting marginal reliability. However, treating the ratings as ordinal rather than nominal—which better captures the structured nature of numeric annotations—significantly improved agreement levels. The Intraclass Correlation Coefficient (ICC) showed moderate reliability (0.462 for semantic, 0.491 for syntactic, both highly significant). Weighted Cohen’s kappa revealed moderate agreement between annotators 1 and 3, while the other pairs showed more variability. These findings highlight the subjectivity and cultural complexity of idiom interpretation, particularly given that none of the annotators are native English speakers. Refining annotation guidelines and targeted training could further improve inter-rater reliability in future iterations.

---

## ⚠️ Limitations  
While this dataset provides a robust **cross-linguistic annotation** of idioms, it has some limitations:  

1. **Subjectivity in Annotation:** Some idioms have multiple possible equivalents, making annotation inherently subjective.  
2. **Cultural and Regional Variations:** Spanish idioms were chosen to be as **neutral as possible**, but **regional preferences may exist**.  
3. **Dataset Size:** While **145 idioms offer valuable insights**, a larger dataset could improve NLP generalization.  

---

## 📥 Download and Usage  
To use this dataset, clone this repository and access the files:  

```bash
git clone https://github.com/julianaplanas/idioms-annotated
```

---

## 🤝 Contributing  
If you want to contribute by expanding the dataset or improving annotations, please follow these steps:

1. **Fork** the repository.  
2. **Make your changes** (e.g., add new idioms, improve translations).  
3. **Submit a pull request** explaining your modifications.  

All contributions are welcome! Please ensure that your additions follow the **annotation guidelines** and include proper documentation.

---

## 📧 Contact  
For questions, feedback, or collaboration opportunities, please contact:  

**Authors:**  
- 📩 Belén Saavedra  
- 📩 Nagore Bravo  
- 📩 Juliana Planas  

---

### 🚀 Thank You for Using **Idiomatic Bridges**!  
We hope this dataset helps advance **NLP, machine translation, and cross-linguistic idiomatic studies**.  
If you use this dataset in your research, please consider citing it!  

