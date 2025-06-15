# Task 2: Explainable AI-Based Summarizer for Nuclear Reports

## 🔍 Objective
Build a working prototype that:
- Summarizes nuclear incident reports using a pre-trained LLM
- Provides explainability by visualizing input token importance via cross-attention

## 🚀 Tools & Models
- **Transformers**: `facebook/bart-large-cnn`
- **Tokenizer**: `BartTokenizer`
- **Framework**: Hugging Face Transformers
- **Explainability**: Cross-attention averaging and bar chart visualization
- **Platform**: Google Colab

## 🛠️ How to Run
1. Open `summarizer.ipynb` in Google Colab or local Jupyter Notebook
2. Install required libraries:
    ```bash
    pip install transformers torch matplotlib
    ```
3. Run all cells — the summary and attention heatmap will be displayed.

## 🧪 Sample Input

```
On June 5, 2024, Unit 3 experienced a temporary loss of power due to a failed generator control module. 
Operators responded immediately and shifted cooling operations to backup systems. 
No radiation was released. The NRC was notified, and full power was restored within 3 hours. 
Investigation revealed that the failure was due to aged circuit components.
```

## 📋 Sample Output

**Summary**:  
Operators restored power within 3 hours after a module failure. No radiation was released.

**Explainability**:  
Bar chart showing which input tokens were most influential in generating the summary.

## 🔄 Reflection

### ✅ What Worked
- Hugging Face pipelines made summarization fast and easy to prototype.
- Pre-trained BART model produced high-quality summaries from long nuclear-style reports.
- Cross-attention weights were easily extractable using Hugging Face `return_dict_in_generate`.

### ❗ Challenges
- Attention scores are at token-level, not sentence-level, so interpreting sentence importance needed manual review.
- Input token length needed truncation to stay within model limits (1024 tokens).
- Multi-head attention can be overwhelming; had to average for simplicity.

### 💡 What I’d Improve
- Add sentence-level mapping of attention weights.
- Build a Streamlit web interface for real-time summarization + explanation.
- Try fine-tuning the model on real nuclear incident data for better domain adaptation.

## 📸 Screenshot
Include a screenshot of:
- Summary output
- Attention bar chart
