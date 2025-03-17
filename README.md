# 🚀 Multi-Modal AI Compliance & Content Analysis Platform  
**Fine-Tuning LLaVA, Video-LLaMA, and RoBERTa for AI-Powered Compliance Analysis**  

## 📌 Overview  
This project is a **multi-modal AI platform** designed to process and analyze **images, videos, and text for compliance validation**. The system integrates **LLaVA-1.5, Video-LLaMA, and RoBERTa** with **custom fine-tuning techniques** (PEFT, LoRA) to generate **detailed content descriptions** and validate compliance using **NLP-based rule matching and semantic similarity models**.  

## 🔥 Key Features  
✅ **Multi-Modal AI Processing**: Supports **image, video, and text analysis** using LLaVA, Video-LLaMA, and RoBERTa.  
✅ **Fine-Tuned LLMs**: Implements **Low-Rank Adaptation (LoRA) and PEFT** for efficient fine-tuning.  
✅ **4-Bit Quantization & Optimization**: Reduces memory footprint with **BitsAndBytesConfig**.  
✅ **Compliance Validation**: Uses **RoBERTa for hate speech detection** and **MiniLM for semantic similarity matching**.  
✅ **AWS-Integrated Pipeline**: Processes **files stored in S3**, triggered via **AWS Lambda**.  
✅ **Scalable Data Handling**: Custom **PyTorch datasets and data loaders** for **efficient batch processing**.  

## 🏗️ Architecture  

### 1️⃣ **Data Ingestion & Preprocessing**  
- **AWS S3 + EventBridge + Lambda** for event-driven file processing.  
- **Multi-modal dataset handling** with **custom PyTorch DataLoaders**.  

### 2️⃣ **Model Processing Pipeline**  
- **Images** → **LLaVA-1.5** generates rich descriptions.  
- **Videos** → **Video-LLaMA extracts frames** and provides detailed context.  
- **Text** → **RoBERTa detects hate speech**, while **MiniLM ensures contextual similarity**.  

### 3️⃣ **Compliance Evaluation**  
- **Regex-based compliance rules** for instant rule matching.  
- **ML-based classification** using pre-trained models.  
- **Generated outputs** include **detailed descriptions, compliance status, and category tags**.  

### 4️⃣ **Final Response** (Sent to AWS Lambda)  
```json
{
    "file_id": 4,
    "user_id": "1c5046f5-a56c-4559-9a4c-c3ad93d2c590",
    "description": "{generated description}",
    "compliance_status": "True or False",
    "categories": ["Violence", "Hate Speech"]
}
```

## 🛠️ Technologies Used  
- **Deep Learning**: LLaVA-1.5, Video-LLaMA, RoBERTa, MiniLM  
- **Optimization**: LoRA, PEFT, 4-bit Quantization  
- **Cloud**: AWS Lambda, S3, EventBridge  
- **Frameworks**: PyTorch, Transformers, FastAPI  
- **Data Handling**: Custom Datasets, PyTorch DataLoaders  

## 📌 Future Enhancements  
🔹 **Expand compliance rules with GPT-based reasoning**  
🔹 **Enhance video processing with temporal context models**  
🔹 **Implement real-time streaming support**  
