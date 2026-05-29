=============================================================
Topic Modeling & Sentiment Analysis
Ayoob Haroon 
=============================================================

Instructions to Reproduce Results
---------------------------------
1. Environment Setup:
   - Python 3.8+ with Jupyter Notebook / Google Colab.
   - Install dependencies (run the first cell of the notebook):
     !pip install -q transformers datasets sentence-transformers faiss-cpu
     !pip install -q gensim nltk scikit-learn
     !pip install -q torch torchvision --extra-index-url https://download.pytorch.org/whl/cu118
     !pip install -q matplotlib seaborn pandas numpy
     !pip install -q pyLDAvis wordcloud
     !pip install -q accelerate bitsandbytes

2. Dataset:
   - Download the dataset (FinancialPhraseBank-v1.0).
   - Upload the ZIP file when prompted in the notebook, or place it in the same directory and adjust the file name in the code.
   - The script automatically unzips and loads Sentences_75Agree.txt.

3. Execution Order:
   - Run the cells sequentially from top to bottom.
   - The notebook contains clearly labeled sections:
       0. Setup & Imports
       1. Data Preprocessing & EDA
       2. LDA Topic Modeling
       3. Sentiment Analysis (FinBERT, Local LLM, RAG)
       4. Comparative Analysis
       5. Fine-Tuning Decision
   - All plots and evaluation metrics are generated inline.

4. Reproducibility:
   - Random seeds are fixed (SEED=42) for Python's random, NumPy, and PyTorch.
   - The optimal LDA topic number (13) is selected automatically via coherence scores, but the final model uses that fixed number.
   - The three sentiment systems are evaluated on the same train/test split.

5. Outputs:
   - Topic keywords and coherence plot.
   - Confusion matrices for FinBERT, Local LLM, and RAG.
   - Comparative metric table.
   - Final conclusion regarding fine-tuning.

6. Additional Files:
   - The notebook itself contains all code.
   - No fine-tuned model weights are generated (fine-tuning not required).
   - The FAISS index and embeddings are built in memory; they can be saved by uncommenting the relevant lines in the RAG section.
   - The results CSV is not separately saved but can be exported from the pandas DataFrames.

7. Contact:
   For any issues, ayoobharoon@gmail.com.
=============================================================
