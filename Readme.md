# Winston AI MCP Server ⚡️

[![npm version](https://badge.fury.io/js/winston-ai-mcp.svg)](https://badge.fury.io/js/winston-ai-mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js CI](https://github.com/gowinston-ai/winston-ai-mcp-server/actions/workflows/CI.yml/badge.svg)](https://github.com/gowinston-ai/winston-ai-mcp-server/actions/workflows/CI.yml)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)

> **Model Context Protocol (MCP) Server for Winston AI** - the most accurate AI Detector. Detect AI-generated content, plagiarism, and compare texts with ease.

## ✨ Features

### 🔍 AI Text Detection
- **Human vs AI Classification**: Determine if text was written by a human or AI
- **Confidence Scoring**: Get percentage-based confidence scores
- **Sentence-level Analysis**: Identify the most AI-like sentences in your text
- **Multi-language Support**: Works with text in various languages

### 🖼️ AI Image Detection
- **Image Analysis**: Detect AI-generated images using advanced ML models
- **Metadata Verification**: Analyze image metadata and EXIF data
- **Watermark Detection**: Identify AI watermarks and their issuers
- **Multiple Formats**: Supports JPG, JPEG, PNG, and WEBP formats

### 📝 Plagiarism Detection
- **Internet-wide Scanning**: Check against billions of web pages
- **Source Identification**: Find and list original sources
- **Detailed Reports**: Get comprehensive plagiarism analysis
- **Academic & Professional Use**: Perfect for content verification

### 🔄 Text Comparison
- **Similarity Analysis**: Compare two texts for similarities
- **Word-level Matching**: Detailed breakdown of matching content
- **Percentage Scoring**: Get precise similarity percentages
- **Bidirectional Analysis**: Compare both directions

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- Winston AI API Key ([Get one here](https://dev.gowinston.ai))

## 🛠️ Development

### Running with npx 🔋
```
env WINSTONAI_API_KEY=your-api-key npx -y winston-ai-mcp
```

### Building from Source

```bash
# Clone the repository
git clone https://github.com/gowinston-ai/winston-ai-mcp-server.git
cd winston-ai-mcp-server

# Install dependencies
npm install

# Build the project and start the server
npm run mcp-start
```

### Environment Setup
Create a `.env` file in your project root:

```env
WINSTONAI_API_KEY=your_actual_api_key_here
```

## 📦 Docker Support

Build and run with Docker:

```bash
# Build the image
docker build -t winston-ai-mcp .

# Run the container
docker run -e WINSTONAI_API_KEY=your_api_key winston-ai-mcp
```

## 📋 Available Scripts

- `npm run build` - Compile TypeScript to JavaScript
- `npm start` - Start the MCP server
- `npm run mcp-start` - Compile TypeScript to JavaScript and Start the MCP server
- `npm run lint` - Run ESLint for code quality
- `npm run format` - Format code with Prettier

## 🔧 Configuration

### For Claude Desktop

Add to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "winston-ai-mcp": {
      "command": "npx",
      "args": ["-y", "winston-ai-mcp"],
      "env": {
        "WINSTONAI_API_KEY": "your-api-key"
      }
    }
  }
}
```

### For Cursor IDE

Add to your Cursor configuration:

```json
{
  "mcpServers": {
    "winston-ai-mcp": {
      "command": "npx",
      "args": ["-y", "winston-ai-mcp"],
      "env": {
        "WINSTONAI_API_KEY": "your-api-key"
      }
    }
  }
}
```

## 📋 API Reference

### AI Text Detection
```typescript
{
  "text": "Your text to analyze (600+ characters recommended)",
  "file": "(optional) A file to scan. If you supply a file, the API will scan the content of the file. The file must be in plain .pdf, .doc or .docx format.",
  "website": "(optional) A website URL to scan. If you supply a website, the API will fetch the content of the website and scan it. The website must be publicly accessible."
}
```

### AI Image Detection
```typescript
{
  "url": "https://example.com/image.jpg"
}
```

### Plagiarism Detection
```typescript
{
  "text": "Text to check for plagiarism",
  "language": "en", // optional, default: "en"
  "country": "us"   // optional, default: "us"
}
```

### Text Comparison
```typescript
{
  "text1": "First text to compare",
  "text2": "Second text to compare"
}
```

## 🤝 Contributing

We welcome contributions!

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Links

- **Winston AI Website**: [https://gowinston.ai](https://gowinston.ai)
- **API Documentation**: [https://dev.gowinston.ai](https://dev.gowinston.ai)
- **MCP Protocol**: [https://modelcontextprotocol.io](https://modelcontextprotocol.io)
- **GitHub Repository**: [https://github.com/gowinston-ai/winston-ai-mcp-server](https://github.com/gowinston-ai/winston-ai-mcp-server)

## ⭐ Support

If you find this project helpful, please give it a star on GitHub!

---

**Made with ❤️ by the Winston AI Team**
