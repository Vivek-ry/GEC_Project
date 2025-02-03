## 📂 **Dataset**

The dataset used for training is publicly available on **Kaggle**.

🔗 **[Click here to access the C4_200M Dataset](https://www.kaggle.com/datasets/dariocioni/c4200m/data?select=C4_200M.tsv-00000-of-00010)**

📌 **Dataset Overview:**
- **18.4M sentence pairs** (incorrect → correct)
- Covers **diverse grammatical structures & writing styles**
- Extracted from **web-sourced text**, ensuring real-world grammar variations

## 📖 **About Dataset**
Grammar Error Correction synthetic dataset consisting of **185 million sentence pairs**, created using a **Tagged Corruption model** on Google's **C4 dataset**.

This version of the dataset was extracted from **Li Liwei's HuggingFace dataset** and converted to **TSV format**.

The **corruption edits** by **Felix Stahlberg and Shankar Kumar** are licensed under **CC BY 4.0**. The **C4 dataset** was released by **AllenAI** under the terms of **ODC-BY**.

By using this dataset, you are also bound by the **Common Crawl terms of use** in respect of the content contained in the dataset.

## 📁 **Format**
This dataset is converted to **Parquet format**, but a **TSV format** is available in previous versions. The reason for the conversion was the **poor performance** in accessing each file. 

🔹 **Dataset Details:**
- Available in **TSV format**, split into **10 files**, each containing approximately **18M samples**.
- Each sample consists of **incorrect and corrected** sentence pairs.

| **Incorrect** | **Corrected** |
|--------------|-------------|
| Much many brands and sellers still in the market. | Many brands and sellers still in the market. |
| She likes playing in park and come here every week | She likes playing in the park and comes here every week |

## 🛠 **Usage**
A **notebook** demonstrating **Grammar Error Correction** using a **seq2seq architecture** (BERT & LSTM) will be released soon. Meanwhile, you can build your own model!

This dataset can be used to train **sequence-to-sequence models**, based on an **encoder-decoder approach**.

🔹 **Related Tutorials:**
- [NLP from Scratch: Translation with a Seq2Seq Network and Attention](https://pytorch.org/tutorials/intermediate/seq2seq_translation_tutorial.html)
- [Language Translation with nn.Transformers and TorchText](https://pytorch.org/tutorials/beginner/transformer_tutorial.html)
- [Grammar Error Correction Example](https://github.com/google-research-datasets/C4_200M-synthetic-dataset-for-grammatical-error-correction)

## 🙌 **Acknowledgments**
Thanks to the dataset creators **Felix Stahlberg and Shankar Kumar**, and to **Li Liwei** for first providing access to the processed dataset.

## 🔗 **References**
- 📄 **Paper:** [ACL Anthology](https://aclanthology.org/2021.bea-1.4/)
- 🏗 **GitHub:** [C4_200M Dataset](https://github.com/google-research-datasets/C4_200M-synthetic-dataset-for-grammatical-error-correction)
- 📰 **Article:** [Google AI Blog](https://ai.googleblog.com/2021/08/the-c4200m-synthetic-dataset-for.html)
- 📚 **Google's C4 Dataset:** [TensorFlow Dataset](https://www.tensorflow.org/datasets/catalog/c4)
- 📂 **Li Liwei Kaggle Dataset (TensorFlow format):** [Kaggle](https://www.kaggle.com/datasets/a0155991rliwei/c4-200m)
- 🔖 **Correction Labels:** [Kaggle](https://www.kaggle.com/datasets/felixstahlberg/the-c4-200m-dataset-for-gec)
