# 📝 Grammatical Error Correction (GEC) using T5 Transformer  
📌 **Fixing grammar with AI – A Deep Learning Approach**

## 🌟 Overview  
Have you ever encountered sentences like *"He go to school every day."* and wished there was an **AI-powered** tool that could instantly correct it to *"He goes to school every day."*?  

This project does exactly that! 🎯  

We built an **AI-driven Grammatical Error Correction (GEC) model** using the **T5 Transformer** – a powerful **sequence-to-sequence** architecture that understands sentence structure and **fixes grammatical errors with high accuracy**.  

Unlike traditional **rule-based** grammar checkers, this **deep learning model**:  
✔ Understands **context and sentence structure** 🧠  
✔ Corrects **complex grammatical errors** 📚  
✔ Adapts to **real-world language use** ✍  

---

## 🚀 Key Features  
- 🔹 **Context-aware grammar correction** using the **T5 Transformer**  
- 🔹 **Fine-tuned on the massive** C4_200M **dataset** (~18.4M sentences)  
- 🔹 **Handles diverse errors:** verb tense, punctuation, subject-verb agreement, word choice  
- 🔹 **Outperforms rule-based grammar checkers** 🚀  
- 🔹 **Achieves high evaluation scores** (ROUGE-1: **71.69**, ROUGE-2: **61.69**, ROUGE-L: **70.96**)  

---

## 📊 Why This Project?  
Grammar correction is **more than just fixing typos**!  
Traditional **rule-based** systems (like Grammarly's basic mode) often fail when dealing with **complex sentence structures**.  

✔ Example:  
> ❌ "She has went to the market."  
> ✅ "She has gone to the market."  

Our model **learns from real-world text data** and understands context, allowing it to correct **grammatical mistakes with precision**.  

---

## 📌 How It Works  

### 💡 Step 1: Data Processing  
- The **C4_200M dataset** is preprocessed, removing noise and inconsistencies.  
- Sentences are tokenized using the **T5 tokenizer** for compatibility with the model.  

### 💡 Step 2: Model Training  
- We fine-tuned the **T5-base Transformer** on incorrect-correct sentence pairs.  
- Training was optimized using **Hugging Face's Transformers library**.  
- Key hyperparameters:  
  - **Learning Rate:** `2e-5`  
  - **Batch Size:** `16`  
  - **Epochs:** `1` (Due to dataset size)  

### 💡 Step 3: Evaluation & Testing  
- Performance is measured using **ROUGE metrics**.  
- Comparison with **rule-based grammar checkers** highlights our model's **superiority**.  

### 💡 Step 4: Real-World Usage  
- A simple **Python script or API** can be used to integrate the model into applications like **Grammarly, MS Word, or chatbots**.  

---

## 📈 Results  

### 📊 Performance Metrics  
| Metric  | Score |
|---------|------|
| **ROUGE-1** (Unigram Overlap) | **71.69** |
| **ROUGE-2** (Bigram Overlap) | **61.69** |
| **ROUGE-L** (Longest Common Subsequence) | **70.96** |

### 📌 Comparison with Rule-Based Systems  
✔ **T5 Model:** ✅ **Understands sentence structure & context**  
✔ **Rule-Based:** ❌ **Fails with ambiguous sentences**  

### 💡 Success Example  
> ❌ **"I am interest to learn."**  
> ✅ **"I am interested in learning."**  

### 💡 Limitation Example  
> ❌ **"I like play soccer."**  
> ✅ **"I like playing soccer too."** (*Unnecessary addition of "too"*)  
---

## 🛠️ Installation & Setup  

### 🔧 1. Clone this Repository  
```bash
git clone https://github.com/Vivek-ry/GEC_Project.git
cd GEC_Project
```

### 📦 2. Install Dependencies  
```bash
pip install transformers datasets torch pandas numpy scikit-learn
```

### ▶️ 3. Run the Model  
```python
# Open the Jupyter Notebook
jupyter notebook GEC_project.ipynb
```

### 🚀 4. Use the Model  
```python
from transformers import T5Tokenizer, T5ForConditionalGeneration

tokenizer = T5Tokenizer.from_pretrained("t5-base")
model = T5ForConditionalGeneration.from_pretrained("your_trained_model_path")

def correct_grammar(sentence):
    input_text = "fix grammar: " + sentence
    inputs = tokenizer(input_text, return_tensors="pt")
    outputs = model.generate(**inputs)
    return tokenizer.decode(outputs[0], skip_special_tokens=True)

# Test it out!
print(correct_grammar("She go to the market every day."))
```

---

## 📂 Repository Structure  

```
📁 GEC_Project
├── 📜 GEC_project.ipynb  # Jupyter Notebook with code
├── 📜 dataset/           # C4_200M dataset (link provided)
├── 📜 results/           # Evaluation reports & analysis
└── 📜 README.md          # You are here!
```

---

## 📎 Dataset  
The dataset used for training is publicly available on **Kaggle**:  
🔗 [C4_200M Dataset](https://www.kaggle.com/datasets/dariocioni/c4200m/data?select=C4_200M.tsv-00000-of-00010)  

📌 **Contains:**  
✔ **18.4M sentence pairs** (incorrect → correct)  
✔ Covers **diverse grammatical structures & writing styles**  

---

## 🔮 Future Improvements  

🔹 **Fine-tune the model on domain-specific datasets** (e.g., legal, medical, academic writing)  
🔹 **Introduce user feedback learning** to refine grammar corrections based on individual preferences  
🔹 **Incorporate semantic understanding** to handle ambiguous sentences better  
🔹 **Deploy as an API or integrate with productivity tools** (Google Docs, Grammarly, etc.)  

---

## 🤝 Contributing  

💡 Found a bug? Want to improve the model? Contributions are welcome!  

1. Fork the repository  
2. Create a feature branch (`git checkout -b feature-name`)  
3. Commit changes (`git commit -m "Add feature"`)  
4. Push to your branch (`git push origin feature-name`)  
5. Open a Pull Request  

---

## 📜 References & Credits  

📚 **Key Research Papers:**  
- **Attention Is All You Need** – Vaswani et al. (2017)  
- **Exploring the Limits of Transfer Learning with T5** – Raffel et al. (2020)  
- **Grammatical Error Correction BEA-2019** – Bryant et al. (2019)  

---

## ✨ Authors  

👤 **Vivekananda Reddy Arekatla**  

👤 **Sai Revanth Myneni**

📌 **GitHub Repository**: [GEC Project](https://github.com/Vivek-ry/GEC_Project)  

---

⭐ **If you find this project useful, don’t forget to star the repo!** 🚀
