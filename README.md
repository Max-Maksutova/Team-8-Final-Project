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

![VAE Diagram](link-to-vae-image)

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

