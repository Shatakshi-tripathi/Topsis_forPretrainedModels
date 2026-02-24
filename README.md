<img width="724" height="568" alt="image" src="https://github.com/user-attachments/assets/5a03d749-9295-49f5-9a04-0cc20e72736c" />**TOPSIS Analysis of Pretrained Models**

**Project Overview**

This project evaluates multiple pretrained machine learning models using the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) multi-criteria decision-making method.

Instead of selecting models based on a single metric, this project:

- Compares pretrained models across multiple performance criteria
- Applies TOPSIS ranking methodology
- Calculates ideal best and worst solutions
- Produces a final ranking score
- Helps identify the most suitable pretrained model objectively

This approach is useful when model selection depends on several performance factors simultaneously.

---

**Problem Statement**

Selecting the best pretrained model is challenging because performance depends on multiple factors such as:

- Accuracy
- Computational efficiency
- Model complexity
- Error metrics

This project uses the TOPSIS decision-making technique to rank pretrained models based on multiple evaluation criteria.

---

**Methodology**

**1. Selection of Pretrained Models**

Multiple pretrained models were evaluated. These models were compared based on predefined performance metrics obtained from experiments or existing benchmarks.

Examples of criteria:

- Accuracy / Performance score
- Error rate
- Computational cost
- Model efficiency

---

**2.TOPSIS Method Steps**

**Step 1 — Create Decision Matrix**

A matrix was constructed where:

- Rows = Models
- Columns = Performance Criteria

This matrix represents how each model performs across different metrics.

**Step 2 — Normalization**

The decision matrix was normalized to eliminate scale differences between criteria.

Formula used:

Normalized Value = Value / √(Sum of Squares of Column)

This ensures fair comparison across metrics.

**Step 3 — Weight Assignment**

Weights were assigned to each criterion depending on importance.

Examples:

- Higher weight for accuracy
- Moderate weight for efficiency
- Lower weight for computational cost (depending on scenario)

**Step 4 — Weighted Normalized Matrix**

Normalized values were multiplied by corresponding weights to reflect importance.

**Step 5 — Identify Ideal Best & Worst Solutions**

- Ideal Best → Highest desirable values
- Ideal Worst → Lowest desirable values

These serve as reference points for ranking.

**Step 6 — Distance Calculation**

Euclidean distance was calculated:

- Distance from ideal best
- Distance from ideal worst

**Step 7 — TOPSIS Score Calculation**

Final score:

Score = Distance from Worst / (Distance from Best + Distance from Worst)

Higher score → Better model.

---

**Results**

**Model Ranking Table (TOPSIS Results)**

| Model       | TOPSIS Score | Rank |
|-------------|-------------|------|
| DistilGPT2  | 0.697543    | 1 |
| GPT2        | 0.696224    | 2 |
| T5          | 0.526029    | 3 |
| BART        | 0.337649    | 4 |
| GPT-Neo     | 0.323040    | 5 |


**Result Interpretation**

**Key Observations:**

- **DistilGPT2 achieved the highest TOPSIS score**, making it the most balanced model across all evaluation criteria.
- **GPT2 ranked second**, performing very closely to DistilGPT2.
- **T5 showed moderate performance**, indicating acceptable but not optimal balance.
- **BART and GPT-Neo ranked lower**, suggesting comparatively weaker performance across selected metrics.

Overall, lighter transformer-based models (like DistilGPT2) showed strong performance when multiple criteria such as efficiency, accuracy, and computational cost were considered together.

---

**TOPSIS Ranking Visualization**
**Graph Discussion**

The graph shows the TOPSIS scores of different pretrained text generation models.

- **DistilGPT2 and GPT2 achieved the highest scores (~0.69)**, indicating the best overall balance across evaluation criteria.  
- **T5 shows moderate performance (~0.53)**.  
- **BART and GPT-Neo scored lower (~0.33)**, suggesting comparatively weaker performance.

Overall, the results indicate that optimized transformer models like DistilGPT2 provide better performance when multiple evaluation factors are considered.

--- 

**Technologies Used**

- Python
- NumPy
- Pandas
- Scikit-learn
- Matplotlib / Visualization Libraries
- TOPSIS Method Implementation

---

**Conclusion**

This project demonstrates how the TOPSIS multi-criteria decision-making method can be used to:

- Evaluate pretrained machine learning models
- Perform objective ranking
- Support model selection decisions

The approach ensures balanced evaluation rather than relying on a single performance metric.

---
