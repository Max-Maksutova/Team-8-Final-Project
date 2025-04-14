# Synthetic Data for Privacy-Preserving AI Development
**Project Report** 

---

## 🧠 Why This Project Matters

Synthetic data is revolutionizing the way businesses handle data privacy, model training, and cross-functional collaboration. By creating artificial datasets that maintain the statistical properties of real-world data, organizations can unlock innovation without breaching privacy or regulatory compliance.

![Synthetic Data](https://www.k2view.com/hubfs/Synthetic%20data%20use%20cases.jpg)

---

## 👥 Author List

- [Max Maksutova](https://github.com/Max-Maksutova/Introduction/blob/main/README.md)  
- [Mollie Schuma](https://github.com/mfschuma/About-Me-)  
- [Nicole Sellers](https://github.com/nlsellers/Introduction)  
- [Sarah Wozniak](https://github.com/danarepo)  

---

## 🎯 Project Scope

This project explores the **generation of synthetic data for enterprise applications**, focusing specifically on:
- Developing and comparing data generators (GANs, VAEs, LLMs)
- Evaluating the utility of synthetic data using similarity metrics
- Applying synthetic data to high-sensitivity industries (e.g., finance)
- Emphasizing privacy-preservation, model utility, and responsible AI

Our primary dataset examples center around **financial services and synthetic equity markets**, drawing from publicly available resources and research by **J.P. Morgan AI Research** and **Gretel.ai**.

---

## 🔍 Project Details

### 📊 What is Synthetic Data?

Artificially generated data that mimics the statistical properties of real data, used to replace or augment real-world datasets.

**Why is it important for businesses?**
- Real data is often sensitive, limited, or inaccessible
- Synthetic data enables:
  - Faster AI development
  - Cross-team collaboration without compliance risk
  - Innovation in regulated sectors

**Benefits:**
- Enhances data privacy
- Reduces regulatory barriers
- Supports scalable data augmentation
 
**Drawbacks:**
- May exclude rare edge cases
- Can introduce unrealistic patterns
- Hard to validate effectiveness

---

### ⚙️ How Synthetic Data is Generated

#### 1. Analyze Real Data *(Optional)*  
Collect, clean, and analyze real data to understand its structure and biases.

#### 2. Develop Generator

##### **VAE (Variational Autoencoder)**  
Encodes real data into low-dimensional space and decodes to reconstruct similar data.

![VAE Diagram](data:image/png;base64,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)

##### **GAN (Generative Adversarial Network)**  
Two networks: generator vs. discriminator. Generator improves to fool the discriminator, leading to realistic outputs.

![GAN Diagram](link-to-gan-image)

##### **LLM (Large Language Model)**  
Used for generating synthetic text data. Trained on large corpora to replicate real-world linguistic structures.

![LLM Diagram](link-to-llm-image)

---

### 🏗️ Generation Process

1. **Compute metrics for real data**  
2. **Train the generator**  
3. **Generate synthetic data**  
4. **Compute metrics for synthetic data**  
5. **Compare and refine**

![Data Generation Pipeline](link-to-pipeline-image)

#### Refinement Goals:
- **Avoid Overfitting**:  
  > Avoid duplicating real data  
- **Avoid Underfitting**:  
  > Ensure synthetic data reflects realistic variety

![Overfitting vs Underfitting](link-to-over-under-fitting-image)

---

### 💼 Applications & Examples

#### 🔐 Anti-Money Laundering (J.P. Morgan)  
Synthetic sequences of banking actions (e.g., account opening, transfers, purchases)

![AML Dataset Visual](link-to-aml-image)

#### 📈 Synthetic Equity Market Data  
Simulated spot and option prices  
- Based on Bloomberg market data  
- Reconstructed using deep learning models

![Market Dataset Visual](link-to-equity-image)

#### 🧾 Customer Journey Events  
Sequences of retail banking actions like ATM withdrawals and app usage

![Customer Journey Image](link-to-customer-journey-image)

#### 🤖 Gretel.ai Use Cases:
- **Synthetic Customer Profiles**
- **Synthetic Healthcare Records**
- **Synthetic Financial Transactions**
- **Time-Series Sensor Data**
- **Synthetic Chat Conversations**

![Gretel Data Samples](link-to-gretel-samples)

---

## 🔮 What's Next?

- Expand application into healthcare and legal domains
- Develop automatic privacy metric scoring system
- Research new forms of generative architectures (e.g., Diffusion models)
- Explore open-source synthetic datasets for public benchmarking

---

## 🤖 Responsible AI Considerations

- **Privacy Guarantees**: Techniques like differential privacy should be implemented to ensure no sensitive information is leaked
- **Bias Awareness**: Synthetic data must be tested for inherited biases
- **Explainability**: Models generating synthetic data should be interpretable
- **Compliance**: Regulatory frameworks (e.g., GDPR, HIPAA) must guide data generation processes

---

## 📚 References
### Research

1. **J.P. Morgan AI Research - Synthetic Data for Financial Services**  
   [https://www.jpmorgan.com/technology/artificial-intelligence/synthetic-data](https://www.jpmorgan.com/technology/artificial-intelligence/synthetic-data)

2. **Gretel.ai: The Synthetic Data Platform**  
   [https://gretel.ai](https://gretel.ai)

3. **[Research Paper]**  
   *Title:* “Synthetic Data: Opening the Gates to Privacy-Preserving AI”  
   *Authors:* Lokhov, Andrei et al.  
   *Published:* 2022  
   *arXiv:* [2205.03257](https://arxiv.org/abs/2205.03257)

### Images

1. **J.P. Morgan AI Research - Synthetic Data for Financial Services**  
   [https://www.jpmorgan.com/technology/artificial-intelligence/synthetic-data](https://www.jpmorgan.com/technology/artificial-intelligence/synthetic-data)

2. **Gretel.ai: The Synthetic Data Platform**  
   [https://gretel.ai](https://gretel.ai)

3. **[Research Paper]**  
   *Title:* “Synthetic Data: Opening the Gates to Privacy-Preserving AI”  
   *Authors:* Lokhov, Andrei et al.  
   *Published:* 2022  
   *arXiv:* [2205.03257](https://arxiv.org/abs/2205.03257)

---

> _This README is part of the MSBA Team 8 Final Project on Synthetic Data for Privacy-Preserving AI Development. For code, datasets, and demos, please refer to the repository directories._

