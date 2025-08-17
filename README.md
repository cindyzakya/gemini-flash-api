# Gemini AI Integration with ExpressJS

This repository demonstrates how to integrate **Google's Gemini 2.5 Flash AI** into a **RESTful API** using **Node.js + ExpressJS**, handling **multimodal inputs** such as text, images, documents, and audio.

It serves as a foundation for building AI-powered APIs capable of analyzing, describing, or transcribing real-world content.

---

## 🚀 Features
* **Text generation** from prompts
* **Image-based input processing**
* **Document-based input processing**
* **Audio-based input processing**
* **Multimodal input** combining files and prompts
* Secure API key handling

---

## 🛠️ Setup
1. Clone the repository:

```bash
git clone https://github.com/cindyzakya/gemini-flash-api.git
cd gemini-flash-api
```

2. Install dependencies:

```bash
npm init -y
```
```bash
npm install express dotenv @google/genai multer
```
```bash
npm install nodemon -g
```

3. Create a `.env` file with your Gemini API key:

```env
GEMINI_API_KEY=your_api_key_here
```

4. Start the server:

```bash
nodemon index.js
```

---

## 📡 API Endpoints
### 1. Generate Text
* **Endpoint:** `POST /generate-text`
* **Description:** Send text prompts to Gemini and receive AI-generated responses.
* **Body Example (JSON):**

```json
{
  "prompt": "Explain why the sky is blue in simple terms."
}
```

---

### 2. Generate From Image
* **Endpoint:** `POST /generate-from-image`
* **Description:** Upload an image file (PNG) and get AI-generated content using `imageToGenerativePart()`.
* **Body Example (multipart/form-data):**

```
Key: image
Value: <your-image-file>
```

---

### 3. Generate From Document
* **Endpoint:** `POST /generate-from-document`
* **Description:** Upload a document (PDF) encoded in Base64 for AI processing.
* **Body Example (multipart/form-data):**

```
Key: document
Value: <your-document-file>
```

---

### 4. Generate From Audio
* **Endpoint:** `POST /generate-from-audio`
* **Description:** Upload an audio file, converted to Base64, for transcription or analysis.
* **Body Example (multipart/form-data):**

```
Key: audio
Value: <your-audio-file>
```

---

## 🔑 Key Learnings
* Setup Node.js + ExpressJS with Gemini 2.5 Flash
* Secure API key management with `.env`
* Handling multimodal inputs for AI endpoints
* Building scalable, AI-powered RESTful APIs
