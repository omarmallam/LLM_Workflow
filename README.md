# LLM Workflows: Content Repurposing with AI

![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)  
![License](https://img.shields.io/badge/License-MIT-green.svg)  
![Submission Date](https://img.shields.io/badge/Submitted-March%2023%202025-orange.svg)

## Overview

`LLM_Workflows.py` is a Python-based system designed to repurpose blog content into multiple formats using AI-driven workflows. Developed for a coding challenge, it showcases three core approaches—Basic Pipeline, Reflexion Workflow, and Agent-Driven Workflow—alongside a bonus comparative evaluation system. 

Powered by a Large Language Model (LLM), this tool extracts key points, generates summaries, creates social media posts, and composes email newsletters, demonstrating automation and adaptability in content transformation.

## Features

### Core Workflows

#### 1. Basic Pipeline Workflow 
A straightforward linear process for quick content transformation:
- Extracts key points
- Generates a summary
- Creates social media posts (Twitter, LinkedIn, Facebook)
- Composes an email newsletter

#### 2. Reflexion Workflow 
Enhances quality through self-correction:
- Iteratively refines content (up to 3 iterations) until quality ≥ 0.8
- Ensures polished, high-quality outputs

#### 3. Agent-Driven Workflow 
A modular, agent-based approach:
- Utilizes specialized agents:
  - **Extractor** (key points)
  - **Summarizer**
  - **Social Media Creator**
  - **Email Composer**
- Offers a flexible and scalable design

### Bonus Challenge 

#### **Comparative Evaluation System**
- Processes a blog post through all workflows
- Evaluates output quality (scores 0-1, provides feedback)
- Compares strengths and weaknesses via LLM analysis

### Technical Highlights

- **LLM Integration**: Supports NGU, GROQ, OpenAI, and OPTOGPT via `.env` configuration
- **Robust Parsing**: Handles varied LLM outputs with fallback mechanisms
- **Dynamic Evaluation**: Uses an LLM to assess clarity, relevance, and appropriateness

## Installation & Setup

### **Requirements**
- **Python**: 3.7 or higher
- **Dependencies**: Install required libraries using:
  ```bash
  pip install -r requirements.txt
  ```

### **Configuration**
Create a `.env` file in the root directory with your LLM API details:
```ini
MODEL_SERVER=NGU
NGU_API_KEY=your_ngu_api_key
NGU_BASE_URL=your_ngu_base_url
NGU_MODEL=your_ngu_model
```

### **Input Preparation**
Prepare a sample blog post in JSON format (`sample_blog_post.json`):
```json
{
  "title": "The Impact of Artificial Intelligence on Modern Healthcare",
  "content": "Artificial intelligence (AI) is revolutionizing healthcare..."
}
```

### **Virtual Environment Setup **
For an isolated Python environment:
```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate    # Windows
```

## Usage
To run the script and process a blog post:
```bash
python LLM_Workflows.py --input sample_blog_post.json
```


