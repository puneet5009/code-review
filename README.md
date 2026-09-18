# AI Code Reviewer

An AI-powered code review application that analyzes source code and provides feedback on code quality, bugs, performance, security, maintainability, and best practices.

## 🚀 Features

* AI-powered code review
* Code editor with syntax highlighting
* Detailed review and improvement suggestions
* Bug and logical error detection
* Performance and optimization suggestions
* Security issue identification
* Clean and responsive interface
* Markdown-formatted AI responses

## 🛠️ Tech Stack

### Frontend

* React
* Vite
* Axios
* Prism.js
* React Markdown
* Rehype Highlight
* React Simple Code Editor

### Backend

* Node.js
* Express.js
* Google Gemini API
* CORS
* dotenv

## 📁 Project Structure

```text
code-review-main/
│
├── Frontend/
│   ├── public/
│   ├── src/
│   │   ├── App.jsx
│   │   ├── App.css
│   │   ├── index.css
│   │   └── main.jsx
│   ├── index.html
│   ├── package.json
│   └── vite.config.js
│
├── BackEnd/
│   ├── src/
│   │   ├── controllers/
│   │   │   └── ai.controller.js
│   │   ├── routes/
│   │   │   └── ai.routes.js
│   │   └── services/
│   │       └── ai.service.js
│   ├── server.js
│   └── package.json
│
├── .gitignore
└── README.md
```

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/puneet5009/code-review.git
```

Navigate into the project:

```bash
cd code-review
```

### 2. Install Backend Dependencies

```bash
cd BackEnd
npm install
```

### 3. Configure Environment Variables

Create a `.env` file inside the `BackEnd` directory:

```env
GOOGLE_GEMINI_KEY=your_gemini_api_key
```

Do not commit your `.env` file to GitHub.

### 4. Start the Backend

From the `BackEnd` directory:

```bash
node server.js
```

The backend will run on:

```text
http://localhost:3000
```

### 5. Install Frontend Dependencies

Open another terminal:

```bash
cd Frontend
npm install
```

### 6. Start the Frontend

```bash
npm run dev
```

The frontend will run on:

```text
http://localhost:5173
```

## 🔑 API

### Review Code

**Endpoint**

```text
POST /ai/get-review
```

**Request Body**

```json
{
  "code": "function sum(a, b) { return a + b; }"
}
```

The backend sends the submitted code to Google Gemini and returns an AI-generated code review.

## 🔒 Environment Variables

The backend requires:

| Variable            | Description           |
| ------------------- | --------------------- |
| `GOOGLE_GEMINI_KEY` | Google Gemini API key |

Keep API keys private and never commit `.env` files to GitHub.

## 🧪 Example

You can submit code such as:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    if (n % 2 == 0)
        cout << "Even";
    else
        cout << "Odd";

    return 0;
}
```

The AI reviewer analyzes the submitted code and provides feedback and possible improvements.

## 📌 Future Improvements

* User authentication
* Support for multiple programming languages
* Review history
* Downloadable code-review reports
* Streaming AI responses
* Improved error handling
* Deployment with production environment variables
* Rate limiting and API protection

## 👨‍💻 Author

**Puneet Rao**

GitHub:
https://github.com/puneet5009

## 📄 License

This project is available for educational and personal use.
