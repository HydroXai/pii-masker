<h1 align="center" style="border-bottom: none">
    <b>
        PII Masker
    </b>
    <br>
    ⭐️ Your Ultimate Privacy Shield for Text Data ⭐️ <br>
</h1>

<p align="center">
PII Masker is an advanced open-source tool that protects your sensitive data using state-of-the-art AI, powered by DeBERTa-v3
</p>

<p align="center">
<a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License: MIT"></a>
<a href="https://python.org"><img src="https://img.shields.io/badge/python-3.8+-blue.svg" alt="Python: 3.8+"></a>
</p>

<p align="center">
    <a href="#✨-key-features"><b>Features</b></a> •
    <a href="#📦-installation"><b>Installation</b></a> •
    <a href="#🚀-quick-start"><b>Quick Start</b></a> •
    <a href="#🔍-how-it-works"><b>How It Works</b></a> •
    <a href="#🤝-Contributing"><b>Contributing</b></a>
</p>

## ✨ Key Features

* 🔒 **Comprehensive Protection**: Identifies and masks multiple PII types including names, addresses, phone numbers, and more
* 🚀 **High Performance**: Powered by DeBERTa-v3 with 1024 token support for processing longer documents
* 🎯 **Precision Focused**: Advanced NLP model fine-tuned specifically for PII detection
* 📊 **Structured Output**: Get both masked text and structured PII dictionary
* 🔄 **Easy Integration**: Simple Python API for seamless integration into your workflow

## 🚀 Quick Start

```python
from pii_masker import PIIMasker

# Initialize the masker
masker = PIIMasker()

# Mask PII in your text
text = "John Doe's SSN is 123-45-6789 and he lives at 1234 Elm St."
masked_text, pii_dict = masker.mask_pii(text)

print(masked_text)
# Output: "[NAME]'s SSN is [SSN] and he lives at [ADDRESS]"
```

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/pii-masker.git
cd pii-masker
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Download the model:
```bash
# Option 1: Automatic download
python -m pii_masker.download_model

# Option 2: Manual download
# Visit: https://huggingface.co/hydroxai/pii_model_weight
# Place files in: pii-masker/output_model/deberta3base_1024/
```

## 🔍 How It Works

PII Masker employs a sophisticated pipeline powered by DeBERTa-v3:

1. **Tokenization** → Smart text splitting for optimal processing
2. **Model Inference** → AI-powered PII detection
3. **Entity Recognition** → Precise identification of sensitive data
4. **Masking** → Secure replacement of PII with placeholders
5. **Data Extraction** → Structured output for further processing

## 🛠️ Advanced Usage

Check out our detailed examples:
- [Basic PII Masking](examples/basic_usage.py)
- [RAG Integration Example](examples/build_RAG_with_pii_and_milvus.ipynb)
- [Batch Processing](examples/batch_processing.py)

## 🤝 Contributing

Contributions make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.

## 🙏 Acknowledgments

Special thanks to:
- [Microsoft](https://github.com/microsoft/DeBERTa) for the DeBERTa model
- [Hugging Face](https://huggingface.co) for model hosting and transformers library
- All our contributors and supporters

---

<p align="center">
Made with ❤️ for the privacy-conscious developer community
</p>
