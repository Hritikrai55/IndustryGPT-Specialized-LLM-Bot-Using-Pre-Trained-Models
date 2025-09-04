# 🦙 Llama 3 LoRA Fine-Tuning on PDFs

A comprehensive implementation for fine-tuning Meta's Llama 3 8B model using LoRA (Low Rank Adaptation) technique on PDF documents, complete with a Gradio web interface for interactive chat.

- 🎓 [Project Certification](https://verified.sertifier.com/en/verify/48872981049167/)

## 📋 Features

- **PDF Processing**: Extract and chunk text from PDF documents
- **LoRA Fine-tuning**: Memory-efficient fine-tuning using Parameter Efficient Fine-Tuning (PEFT)
- **4-bit Quantization**: Reduced memory usage with `bitsandbytes` integration
- **Gradio Interface**: Interactive web UI for chatting with your fine-tuned model
- **Instruction Dataset Generation**: Automatic conversion of PDF content to instruction-style training data
- **Hugging Face Integration**: Seamless model loading and saving

## 🚀 Getting Started

### Prerequisites

- CUDA-compatible GPU with sufficient VRAM (recommended: 16GB+)
- Python 3.8+
- Hugging Face account with access to Llama 3 models

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd Llama-Finetune
   ```

2. **Install required libraries** (as outlined in the notebook)
   - PyTorch with CUDA support
   - Transformers library
   - PEFT (Parameter Efficient Fine-Tuning)
   - bitsandbytes
   - Gradio
   - PyPDF2/pdfplumber for PDF processing
   - Other dependencies as needed

3. **Hugging Face Authentication**
   - Create a Hugging Face account
   - Accept the Llama 3 license agreement
   - Generate and configure your HF token

## 📁 Project Structure

```
Llama-Finetune/
├── Llama_Finetune.ipynb    # Main notebook with complete pipeline
├── pdfs/                   # Directory for PDF documents
│   └── Attention All You Need.pdf  # Example PDF (Transformer paper)
├── README.md              # This file
└── .git/                  # Git repository
```

## 🔧 Usage

### Step-by-step Process

1. **Environment Setup**
   - Install CUDA-enabled PyTorch
   - Configure required libraries

2. **Hugging Face Login**
   - Authenticate to access gated Llama 3 weights

3. **PDF Processing**
   - Extract text from PDFs in the `pdfs/` directory
   - Chunk content for optimal training

4. **Dataset Creation**
   - Convert PDF chunks to instruction-style JSONL format
   - Prepare data for training

5. **Tokenization**
   - Process text using Llama 3 tokenizer

6. **LoRA Fine-tuning**
   - Fine-tune model using 4-bit quantization
   - Efficient training with minimal memory usage

7. **Inference**
   - Load fine-tuned adapters
   - Test model performance

8. **Gradio Interface**
   - Launch interactive web UI
   - Chat with your fine-tuned model

### Running the Notebook

Open `Llama_Finetune.ipynb` in Jupyter/Google Colab and follow the step-by-step instructions. The notebook is designed to be run sequentially from top to bottom.

## 🤖 Model Information

- **Base Model**: `meta-llama/Meta-Llama-3-8B-Instruct`
- **Fine-tuning Method**: LoRA (Low Rank Adaptation)
- **Quantization**: 4-bit using bitsandbytes
- **Framework**: Hugging Face Transformers + PEFT

## 📚 Sample Data

The repository includes the "Attention Is All You Need" paper as sample PDF data for demonstration purposes. You can replace this with your own PDF documents for domain-specific fine-tuning.

## 🛠️ Technical Details

- **Memory Optimization**: 4-bit quantization reduces VRAM requirements significantly
- **LoRA Configuration**: Efficient adapter-based fine-tuning preserves base model
- **Instruction Format**: Converts PDF content to conversational instruction-response pairs
- **Gradio Integration**: Real-time chat interface for model interaction

## 📝 Notes

- Ensure you have sufficient GPU memory for the model size
- The notebook includes Google Colab compatibility
- Fine-tuning time depends on dataset size and hardware capabilities
- Save your fine-tuned adapters for future use

## 🤝 Contributing

Feel free to submit issues, fork the repository, and create pull requests for improvements.

## 📄 License

This project follows the respective licenses of:
- Meta's Llama 3 (Custom License)
- Hugging Face Transformers (Apache 2.0)
- Other dependencies as per their individual licenses

## 🙏 Acknowledgments

- Meta AI for the Llama 3 model
- Hugging Face for the excellent ecosystem
- The authors of "Attention Is All You Need" for the foundational transformer architecture

## 📞 Contact
- 🌐 [LinkedIn Profile](https://www.linkedin.com/in/hritik-rai-/)
---

**Happy Fine-tuning!** 🚀
