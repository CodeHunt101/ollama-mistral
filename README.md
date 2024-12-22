# Ollama-Mistral API

A simple Express.js API that interfaces with the Mistral language model through Ollama, providing a local alternative to cloud-based LLM services.

## Prerequisites

Before you begin, ensure you have the following installed:

1. [Node.js](https://nodejs.org/) (version 14 or higher)
2. [Ollama](https://ollama.ai/download)
3. Mistral model for Ollama

To install the Mistral model, run:
```bash
ollama pull mistral
```

## Installation

1. Clone the repository:
```bash
git clone [your-repository-url]
cd ollama-mistral
```

2. Install dependencies:
```bash
npm install
```

## Usage

1. Start the server:
```bash
npm start
```

2. The server will start running on `http://localhost:3000`

3. To ask questions, make GET requests to the root endpoint with a `question` parameter:
```
http://localhost:3000/?question=Your-question-here
```

Example using curl:
```bash
curl "http://localhost:3000/?question=What is the capital of France?"
```

## API Endpoints

### GET /
- Query Parameters:
  - `question`: The question you want to ask the model
- Returns: Text response from the Mistral model
- If no question is provided, returns instructions for usage

## Project Structure

```
ollama-mistral/
├── index.js        # Main application file
├── package.json    # Project dependencies and scripts
└── .gitignore     # Git ignore configuration
```

## Dependencies

- express: ^4.19.1
- ollama: ^0.5.0

## Notes

- This application runs completely locally and doesn't require internet access once the model is downloaded
- The Mistral model requires significant disk space and RAM to run effectively
- First-time responses might be slower as the model loads into memory
