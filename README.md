### 📈 **Cyberbullying Detection System**  

This project is an AI-powered **cyberbullying detection system** built with **FastAPI** and **Transformers**. It detects toxic or harmful messages and can be deployed as a REST API.

## 🚀 **Features**  
✔️ **FastAPI** for creating the REST API  
✔️ **Hugging Face Transformers** for NLP  
✔️ **Pre-trained BERT Model** for text classification  
✔️ **Docker Support** (optional)  
✔️ **Easy Deployment** using **Render**  

---

## 🔧 **Installation & Setup**  

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/amitjha1537/Cyberbullying-Detection-System.git
cd Cyberbullying-Detection-System
```

### **2️⃣ Set Up a Virtual Environment (Optional but Recommended)**
```bash
python -m venv venv
source venv/bin/activate   # On macOS/Linux
venv\Scripts\activate      # On Windows
```

### **3️⃣ Install Dependencies**
```bash
pip install -r requirements.txt
```

---

## 🌍 **Running the API Locally**  
```bash
uvicorn main:app --reload
```
🔹 The API will run at `http://127.0.0.1:8000/`  

---

## 🔥 **API Usage**  

### **POST Request (Using Postman or cURL)**  
Send a **POST request** to `/predict` with a **JSON payload**:  

```json
{
  "text": "You are so stupid"
}
```

### **Example cURL Command**
```bash
curl -X 'POST' 'http://127.0.0.1:8000/predict' \
-H 'Content-Type: application/json' \
-d '{"text": "You are so stupid"}'
```

### **Expected Response**  
```json
{
  "prediction": "Cyberbullying",
  "confidence": 0.98
}
```

---

## 🚀 **Deploying to Render**  

### **1️⃣ Create a `requirements.txt` File**  
```bash
pip freeze > requirements.txt
```

### **2️⃣ Create a `render.yaml` File**  
Add this file in the root directory:
```yaml
services:
  - type: web
    name: cyberbullying-api
    env: python
    buildCommand: "pip install -r requirements.txt"
    startCommand: "uvicorn main:app --host 0.0.0.0 --port 10000"
    plan: free
```

### **3️⃣ Push to GitHub**  
```bash
git add .
git commit -m "Deploy API to Render"
git push origin main
```

### **4️⃣ Deploy on Render**  
Go to [Render.com](https://render.com/)  
🔹 **New Web Service → Connect GitHub Repo → Deploy!**  

---

## 🛠 **Contributing**  
Want to improve this project? Contributions are welcome!  
1. **Fork the repository**  
2. **Create a new branch** (`git checkout -b feature-branch`)  
3. **Make your changes**  
4. **Commit the changes** (`git commit -m "Added new feature"`)  
5. **Push the branch** (`git push origin feature-branch`)  
6. **Create a Pull Request!** 🚀  

---

## ⚖️ **License**  
📝 This project is licensed under the **MIT License**.  

