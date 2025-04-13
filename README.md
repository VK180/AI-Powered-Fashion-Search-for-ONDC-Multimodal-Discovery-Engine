### AI-Powered-Fashion-Search-for-ONDC-Multimodal-Discovery-Engine

This project is a multimodal smart product discovery engine developed for the ONDC . It enables users to search for fashion products using natural language, voice commands, or images. The goal is to create an intuitive and intelligent system that enhances product discoverability across ONDC-compatible seller platforms.

### Dataset
The system uses the Fashion Product Images Dataset from Kaggle, which contains two main files: `styles.csv` (product metadata including gender, category, and product names) and `images.csv` (product image links). These were cleaned, merged, and preprocessed to create a unified, searchable dataset. A price column was added using synthetic values since actual prices were not provided.

### Models and Tools Used
- **MiniLM (`all-MiniLM-L6-v2`)**: A lightweight transformer model from HuggingFace used to generate dense embeddings of product descriptions and user queries for semantic similarity.
- **FAISS**: A high-performance similarity search library used to index and retrieve semantically similar products based on vector distance.
- **CLIP (`clip-ViT-B-32`)**: Integrated via SentenceTransformer to enable visual search. User-uploaded product images are encoded and matched against the dataset.
- **Whisper (base)**: OpenAI’s speech-to-text model used for transcribing voice input into text, which is then processed like a regular search query.

### Assumptions Made
- Product prices were not included in the dataset, so they were synthetically generated.

### Executing final.ipynb file
All code is included in a single Jupyter notebook. To test the system:
1. Download the notebook from GitHub
2. Upload it to [Google Colab](https://colab.research.google.com)
3. Run all cells step-by-step
4. Upload the dataset CSV files (`styles.csv` and `images.csv`) when prompted
5. When running the voice or image-based search cells, make sure to upload an audio file (e.g., `.mp3`, `.ogg`) or an image (e.g., `.jpg`, `.png`) as required

### Final Notes
This project shows how a combination of open-source NLP, CV, and speech models can deliver a unified, intelligent discovery engine.
