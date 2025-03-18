
# Bengali Math Olympiad AI Solver 

This repository presents a solution for solving Bengali Math Olympiad problems using AI, combining multiple approaches such as **TIRagent**, **AgenticRAG**, and the **Translation Approach**. The goal is to develop an AI model capable of solving mathematical problems in Bengali, interpreting LaTeX notation, and performing accurate mathematical reasoning.

## Problem Overview

The task involves solving mathematical problems written in Bengali, with LaTeX-style mathematical notation. The dataset consists of 209 training problems from the Bengali Math Olympiad, and 100 test problems. The goal is to develop an AI model capable of accurately solving these problems. The current model can successfully solve **70 out of 100 unknown problems**.

## Approaches Used

### 1. **TIRagent Approach**

The **TIRagent** approach employs a combination of advanced models and hyperparameters to tackle complex mathematical reasoning in Bengali.

#### Model & Framework Used:
   - **Numina Model:** A state-of-the-art model designed for advanced mathematical problem-solving in Bengali.
   - **vLLM (Virtual Large Language Model):** A library used to manage large-scale computations and optimize performance across multiple GPUs.

#### Training & Evaluation:
   - The model is trained on a dataset of 209 Bengali Math Olympiad problems and evaluated using a test set of 100 problems.

### 2. **AgenticRAG Approach (Retrieve-and-Generate)**

The **AgenticRAG** approach enhances **TIRagent** by combining the power of information retrieval and generation.

#### Tools Used:
   - **LangChain, ChatGroq, HuggingFace Embeddings, DuckDuckGoSearch, TavilySearch, Chroma VectorStore:** These tools are used for document retrieval and integrating external knowledge to solve math problems.

#### Workflow:
   - External knowledge is retrieved from search engines and used to generate solutions with the help of model like **Numina**

### 3. **Translation Approach**

The **Translation Approach** leverages machine translation to convert Bengali math problems into English while preserving mathematical expressions written in LaTeX.

#### Key Steps:
   - **Google Translator (via deep-translator):** This library is used to translate the problem text from Bengali to English.
   - **Latex Expression Handling:** The translation process ensures that mathematical expressions written in LaTeX remain unchanged during translation.

#### Workflow:
   - **Translate Bengali Problems:** The Bengali math problems are translated into English, while LaTeX expressions are preserved.
   - **Process Flow:** 
     1. Extract the Bengali text and LaTeX expressions.
     2. Translate the Bengali text to English.
     3. Combine the translated text with the original LaTeX expressions.

### Integration of All Approaches

Each of these approaches—**TIRagent**, **AgenticRAG**, and **Translation Approach**—complements the others, providing a comprehensive framework for solving the Bengali Math Olympiad problems. The **Translation Approach** provides an alternative for translating problems into a widely-used language (English), while **TIRagent** and **AgenticRAG** focus on mathematical reasoning and the use of external knowledge to improve problem-solving capabilities.

## Installation

To set up the environment and run the solution locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/istiakrifti/llms-based-bengali-math-olympiad-solver.git
   cd llms-based-bengali-math-olympiad-solver
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

   Note: The solution uses **vLLM**, **Numina**, **LangChain**, and **deep-translator**, so these libraries must be installed with specific configurations.

## Files and Directories

- `TIRapproach.ipynb`: The main Jupyter notebook containing the **TIRagent** approach, training process, and evaluation steps.
- `AgenticRagWithllama-3.ipynb`: The notebook that integrates the **AgenticRAG** approach with external retrieval tools for enhancing solution generation.
- `NormalTranslatingApproach.ipynb`: The notebook that implements the **Translation Approach** to convert Bengali problems to English while preserving LaTeX expressions.
- `requirements.txt`: File containing the necessary Python libraries and dependencies for the solution.

## Running the Model

To train and test the model using the **TIRagent**, **AgenticRAG**, and **Translation Approaches**, run the provided Jupyter notebooks:

1. Open the notebooks:
   ```bash
   jupyter notebook TIRapproach.ipynb
   jupyter notebook AgenticRagWithllama-3.ipynb
   jupyter notebook NormalTranslatingApproach.ipynb
   ```

2. Follow the instructions inside the notebooks to preprocess the data, train the models, and evaluate their performance on the test set.

## Performance Evaluation

The performance of the **TIRagent**, **AgenticRAG**, and **Translation** models is evaluated based on the following criteria:
- **Correctness:** Accuracy of the solutions generated by the models for the math problems.
- **Efficiency:** The models' ability to run within the time and space constraints provided.
- **Generalization:** The models' ability to solve previously unseen problems from the holdout set.

The model can successfully solve **70 out of 100 unknown problems**.

