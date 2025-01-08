## **Context**
This project was developed **prior to the release of ChatGPT and other advanced generative AI models**, showcasing foundational natural language processing techniques and manual model development. The focus was on leveraging pre-trained transformers like T5 and Spark NLP for solving text summarization and information extraction tasks.

# **Spark NLP for Text Manipulation** ✍️

## **Problem Statement**
In today’s information-driven world, vast amounts of text are generated daily. Reading every article of interest is often impractical due to time constraints. Moreover, extracting specific information from large text corpora can be challenging with conventional search methods. This project aims to address these challenges by building:
1. A **text summarization model** for efficient information distillation.
2. An **information extraction model** to retrieve specific details seamlessly.

---

## **Project Workflow**
### **1. Install Required Software**
Set up the necessary environment to support text processing and modeling using Spark NLP.

### **2. Data Acquisition and Cleaning**
- Dataset: **“All the News”** from Kaggle ([Dataset Link](https://www.kaggle.com/datasets/snapcrack/all-the-news)).
- File Used: `articles1.csv`  
  - Size: **203.54 MB** | Subset Size: **12.6 MB** | Format: `CSV`
- Preprocessing:
  - Removed null values.
  - Cleaned text data to eliminate multiple spaces and other inconsistencies.

### **3. Data Exploration**
Conducted exploratory data analysis (EDA) and visualizations to gain insights into the dataset, including the distribution of article lengths, publication dates, and sources.

### **4. Model Development**
#### **a. Text Summarization**
- **Model Used**: Google T5 (Text-to-Text Transfer Transformer).
  - **T5-Small**: Generated summaries but lacked contextual coherence and usability.
  - **T5-Base**: Produced significantly better summaries but required substantial memory resources.
  - **Challenges**: Memory limitations restricted the use of larger transformer models like BART.

#### **b. Information Extraction**
- **Technique Used**: RegexMatcher from Spark NLP.
  - Successfully extracted structured information based on predefined patterns.
  - Provides a foundation for further development with more sophisticated methods.

### **5. Results and Evaluation**
- **Summarization**: While T5-Base performed reasonably well, room for improvement remains, especially in generating highly coherent and concise summaries for large-scale text.
- **Extraction**: RegexMatcher proved effective but requires refinement and scalability for broader use cases.

---

## **Technical Specifications**
### **Hardware**
- **OS**: Ubuntu 22.04.2 LTS (64-bit) on VMware Workstation Player 17.
- **Processor**: Intel i7-10750H.
- **Memory**: 16GB RAM.

### **Software**
- **Python**: 3.10.6.
- **PySpark**: 3.3.1.
- **Java**: Java 8 (Required for Spark NLP).

---

## **Lessons Learned**
1. **Modeling Challenges**:
   - Smaller transformer models like T5-Small are insufficient for high-quality summarization tasks.
   - Larger models (e.g., T5-Base) offer better performance but require high computational resources.
2. **RegexMatcher**:
   - While effective, regex-based extraction is inherently limited and should be complemented with machine learning or deep learning approaches for broader applications.
3. **Infrastructure**:
   - Managing large datasets and transformer models on limited hardware presents significant challenges, highlighting the need for more robust systems or cloud-based solutions.

---

## **Future Enhancements**
- **Improve Summarization**:
  - Experiment with advanced transformer models like BART or Pegasus on a distributed cloud infrastructure.
  - Fine-tune pre-trained models on domain-specific text for better results.
- **Enhance Information Extraction**:
  - Incorporate named entity recognition (NER) models and knowledge graphs for dynamic and context-aware extraction.
- **Scale Infrastructure**:
  - Transition to scalable environments (e.g., AWS EMR, Databricks) to handle larger datasets and compute-intensive models.
