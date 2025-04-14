# Synthetic Data for Privacy-Preserving AI Development

---

## 🧠 Why This Project Matters

Synthetic data is revolutionizing the way businesses handle data privacy, model training, and cross-functional collaboration. By creating artificial datasets that maintain the statistical properties of real-world data, organizations can unlock innovation without breaching privacy or regulatory compliance.

![Synthetic Data](https://www.k2view.com/hubfs/Synthetic%20data%20use%20cases.jpg)

---

## 👥 Author List

- [Max Maksutova](https://github.com/Max-Maksutova/Introduction/blob/main/README.md)  
- [Mollie Schuma](https://github.com/mfschuma/About-Me-)  
- [Nicole Sellers](https://github.com/nlsellers/Introduction)  
- [Sarah Wozniak](https://github.com/sdwozniak) 

---

## 🎯 Project Scope

This project explores the **generation of synthetic data for enterprise applications**, focusing specifically on:
- Developing and comparing data generators (GANs, VAEs, LLMs)
- Evaluating the utility of synthetic data using similarity metrics
- Applying synthetic data to high-sensitivity industries (e.g., finance)
- Emphasizing privacy-preservation, model utility, and responsible AI

Our primary dataset examples center around **financial services and synthetic equity markets**, drawing from publicly available resources and research by **J.P. Morgan AI Research** and **Gretel.ai**.

In addition, we used **vibe coding** (ie. prompting an AI to write and execute the creation of code) to build an interactive website on the subject of synthetic data  

---

## 🔍 Project Details

### 📊 What is Synthetic Data?

Artificially generated data that mimics the statistical properties of real data, used to replace or augment real-world datasets.
![exSyntheticData](https://dataingovernment.blog.gov.uk/wp-content/uploads/sites/46/2020/08/synthetic_data_image-1536x718.png)

**Why is it important for businesses?**
- Real data is often sensitive, limited, or inaccessible.
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

![VAE Diagram](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/creative-assets/s-migr/ul/g/b6/f4/variational-autoencoder-neural-network.png)

##### **GAN (Generative Adversarial Network)**  
Two networks: generator vs. discriminator. Generator improves to fool the discriminator, leading to realistic outputs.

![GAN Diagram](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*Y_AGVp0EEGEpB1Q25G6edQ.jpeg)

##### **LLM (Large Language Model)**  
Used for generating synthetic text data. Trained on large corpora to replicate real-world linguistic structures.

![LLM Diagram](https://thegradient.pub/content/images/2023/07/llm_first_diagram.png)

#### 3. Create & Compare 
Generate synthetic data using your generator of choice. Then, analyze & compare metrics between your original data and the synthetic data. 

#### 4. Refine Generator
- **Avoid Overfitting**:  
  > Avoid duplicating real data 
- **Avoid Underfitting**:  
  > Ensure synthetic data reflects realistic variety

![Overfitting vs Underfitting](https://miro.medium.com/v2/resize:fit:1100/format:webp/0*xmtcfLquAbwFjvuN)

---

### Example Code for a Synthetic Data Generator in Python 

The following code generates simple synthetic customer data by calling on a pre-established synthetic data library called Faker. 

```{python}
import random
import pandas as pd
import numpy as np
from faker import Faker

# Initialize the Faker library
fake = Faker()

# Set seeds for reproducibility
random.seed(42)
np.random.seed(42)

# Number of synthetic records
num_records = 1000

# Function to generate more realistic synthetic customer data
def generate_data(n):
    data = []
    for _ in range(n):
        name = fake.name()  # Generate full name
        email = fake.email()  # Generate fake email address
        phone = fake.phone_number()  # Generate fake phone number
        city = fake.city()  # Generate random city
        state = fake.state()  # Generate random U.S. state
        age = random.randint(18, 70)  # Random age
        gender = random.choice(['Male', 'Female', 'Non-binary'])  # Random gender
        income = round(np.random.normal(60000, 15000), 2)  # Normal distribution for annual income
        product_interest = random.choice(['Fitness', 'Tech', 'Travel', 'Fashion', 'Home Decor', 'Beauty'])  # Random interest category
        purchased = np.random.choice([0, 1], p=[0.7, 0.3])  # 30% chance of having purchased
        data.append([name, email, phone, city, state, age, gender, income, product_interest, purchased])
    return data

# Define column names
columns = [
    'Name', 'Email', 'Phone', 'City', 'State', 
    'Age', 'Gender', 'Annual_Income', 'Product_Interest', 'Purchased'
]

# Generate and store the data in a DataFrame
synthetic_data = pd.DataFrame(generate_data(num_records), columns=columns)

# Preview the first few rows
print(synthetic_data.head())

# Optional: Save to CSV
synthetic_data.to_csv('enhanced_synthetic_customer_data.csv', index=False)
```
**Example Output**


---

### 💼 Applications & Examples

#### 🔐 Anti-Money Laundering (J.P. Morgan)  
Synthetic sequences of banking actions (e.g., account opening, transfers, purchases)

![AML Dataset Visual](https://www.jpmorgan.com/content/dam/jpm/cib/technology/banners/antimoney-laundering-data.png)

#### 📈 Synthetic Equity Market Data  
Simulated spot and option prices  
- Based on Bloomberg market data  
- Reconstructed using deep learning models

![Market Dataset Visual](https://www.jpmorgan.com/content/dam/jpm/cib/technology/banners/synthetic-equity.JPG)

#### 🧾 Customer Journey Events  
Sequences of retail banking actions like ATM withdrawals and app usage

![Customer Journey Image](https://www.jpmorgan.com/content/dam/jpm/cib/technology/banners/customer-journey-event-data.png)

#### 🤖 Gretel.ai Use Cases:
- **Synthetic Customer Profiles**
- **Synthetic Healthcare Records**
- **Synthetic Financial Transactions**
- **Time-Series Sensor Data**
- **Synthetic Chat Conversations**

![Gretel Data Samples](https://cdn.prod.website-files.com/5ec4696a9b6d337d51632638/641c5aa0be3d60b7e1f76761_RelationalDB.webp)

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

**1. ArXiv - Synthetic Data in Machine Learning**  
- Research Paper: [https://arxiv.org/pdf/2205.03257](https://arxiv.org/pdf/2205.03257)

**2. IBM - Variational Autoencoders**  
- Research: [https://www.ibm.com/think/topics/variational-autoencoder](https://www.ibm.com/think/topics/variational-autoencoder)  
- Image Reference: [IBM VAE Image](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/creative-assets/s-migr/ul/g/b6/f4/variational-autoencoder-neural-network.png)

**3. Medium - Packt - GAN Architecture**  
- Research: [https://medium.com/@Packt_Pub/inside-the-generative-adversarial-networks-gan-architecture-2435afbd6b3b](https://medium.com/@Packt_Pub/inside-the-generative-adversarial-networks-gan-architecture-2435afbd6b3b)  
- Image Reference: [GAN Architecture Image](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*Y_AGVp0EEGEpB1Q25G6edQ.jpeg)

**4. UK Government - Synthetic Data for ML**  
- Research: [https://dataingovernment.blog.gov.uk/2020/08/20/synthetic-data-unlocking-the-power-of-data-and-skills-for-machine-learning/](https://dataingovernment.blog.gov.uk/2020/08/20/synthetic-data-unlocking-the-power-of-data-and-skills-for-machine-learning/)  
- Image Reference: [UK Gov Synthetic Data Image](https://dataingovernment.blog.gov.uk/wp-content/uploads/sites/46/2020/08/synthetic_data_image-1536x718.png)

**5. Regression Visualization**  
- Image Reference Only: [Regression Plot Image](https://dmol.pub/_images/regression_17_0.png)

**6. Medium - Underfitting vs. Overfitting**  
- Research: [https://medium.com/@maheshhkanagavell/understanding-underfitting-and-overfitting-in-data-science-a-comprehensive-guide-with-real-time-b97a5c057779](https://medium.com/@maheshhkanagavell/understanding-underfitting-and-overfitting-in-data-science-a-comprehensive-guide-with-real-time-b97a5c057779)  
- Image Reference: [Under/Overfitting Image](https://miro.medium.com/v2/resize:fit:1100/format:webp/0*xmtcfLquAbwFjvuN)

**7. JPMorgan - Synthetic Data for Anti-Money Laundering**  
- Research: [https://www.jpmorgan.com/technology/artificial-intelligence/initiatives/synthetic-data/anti-money-laundering](https://www.jpmorgan.com/technology/artificial-intelligence/initiatives/synthetic-data/anti-money-laundering)  
- Image Reference: [AML Data Image](https://www.jpmorgan.com/content/dam/jpm/cib/technology/banners/antimoney-laundering-data.png)

**8. O'Reilly - Practical Synthetic Data**  
- Research: [https://www.oreilly.com/library/view/practical-synthetic-data/9781492072737/ch04.html](https://www.oreilly.com/library/view/practical-synthetic-data/9781492072737/ch04.html)  
- Image Reference: [O’Reilly Synthetic Data Image](https://www.oreilly.com/api/v2/epubs/9781492072737/files/assets/psdg_0405.png)

**9. The Gradient - LLMs & Linguistics**  
- Research: [https://thegradient.pub/what-do-llms-know-about-linguistics-it-depends-on-how-you-ask/](https://thegradient.pub/what-do-llms-know-about-linguistics-it-depends-on-how-you-ask/)  
- Image Reference: [LLM Diagram Image](https://thegradient.pub/content/images/2023/07/llm_first_diagram.png)

**10. JPMorgan - Synthetic Equity Market Data**  
- Research: [https://www.jpmorgan.com/technology/artificial-intelligence/initiatives/synthetic-data/synthetic-equity-market-data](https://www.jpmorgan.com/technology/artificial-intelligence/initiatives/synthetic-data/synthetic-equity-market-data)  
- Image Reference: [Synthetic Equity Market Image](https://www.jpmorgan.com/content/dam/jpm/cib/technology/banners/synthetic-equity.JPG)

**11. JPMorgan - Customer Journey Event Data**  
- Research: [https://www.jpmorgan.com/technology/artificial-intelligence/initiatives/synthetic-data/customer-journey-event](https://www.jpmorgan.com/technology/artificial-intelligence/initiatives/synthetic-data/customer-journey-event)  
- Image Reference: [Customer Journey Event Image](https://www.jpmorgan.com/content/dam/jpm/cib/technology/banners/customer-journey-event-data.png)

**12. Gretel AI - Synthetic Relational Databases**  
- Research: [https://gretel.ai/blog/generate-synthetic-databases-with-gretel-relational](https://gretel.ai/blog/generate-synthetic-databases-with-gretel-relational)  
- Image Reference: [Gretel Relational DB Image](https://cdn.prod.website-files.com/5ec4696a9b6d337d51632638/641c5aa0be3d60b7e1f76761_RelationalDB.webp)


---

> _This README is part of the MSBA Team 8 Final Project on Synthetic Data for Privacy-Preserving AI Development. For code, datasets, and demos, please refer to the repository directories._

