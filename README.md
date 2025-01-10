# BrowserAI 🚀

Bring the power of AI directly into your browser! BrowserAI is a lightweight JavaScript library that enables running AI models directly in the browser using WebGPU acceleration.

## ✨ Features

- 🎯 Run AI models directly in the browser - no server required!
- ⚡ WebGPU acceleration for blazing fast inference
- 🔄 Seamless switching between MLC and Transformers engines
- 📦 Pre-configured popular models ready to use
- 🛠️ Easy-to-use API for text generation and more

## 🚀 Quick Start
```
bash
npm install @browserai/browserai
```

OR 
```
bash
yarn add @browserai/browserai
```

### Basic Usage

```javascript
import { BrowserAI } from '@browserai/browserai';

const browserAI = new BrowserAI();

browserAI.loadModel('llama-3.2-1b-instruct');

const response = await browserAI.generateText('Hello, how are you?');
console.log(response);
```


## 📚 Examples

### Text Generation with Custom Parameters
```javascript
const ai = new BrowserAI();
await ai.loadModel('llama-3.2-1b-instruct', {
quantization: 'q4f16_1' // Optimize for size/speed
});
const response = await ai.generateText('Write a short poem about coding', {
temperature: 0.8,
maxTokens: 100
});
```

### Speech Recognition
```javascript
const ai = new BrowserAI();
await ai.loadModel('whisper-tiny-en');
const audioBlob = await ai.stopRecording();
const transcription = await ai.transcribeAudio(audioBlob);
```

### Text-to-Speech
```javascript
const ai = new BrowserAI();
const audioBuffer = await ai.textToSpeech('Hello, how are you today?');
// Play the audio...
```

## 🔧 Supported Models

### MLC Models
- Llama-3.2-1b-Instruct
- SmolLM2-135M-Instruct
- SmolLM2-350M-Instruct

### Transformers Models
- Llama-3.2-1b-Instruct
- Whisper-tiny-en (Speech Recognition)
- SpeechT5-TTS (Text-to-Speech)

## 🗺️ Enhanced Roadmap

### Phase 1: Foundation
- 🎯 Simplified model initialization
- 📊 Basic monitoring and metrics
- 🔍 Simple RAG implementation
- 🛠️ Developer tools integration

### Phase 2: Advanced Features
- 📚 Enhanced RAG capabilities
  - Hybrid search
  - Auto-chunking
  - Source tracking
- 📊 Advanced observability
  - Performance dashboards
  - Memory profiling
  - Error tracking

### Phase 3: Enterprise Features
- 🔐 Security features
- 🌐 Distributed processing
- 📈 Advanced analytics
- 🤝 Multi-model orchestration

## 🤝 Contributing

We welcome contributions! Feel free to:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [MLC AI](https://mlc.ai/) for their incredible mode compilation library and support for webgpu runtime and xgrammar
- [Hugging Face](https://huggingface.co/) for their Transformers.js library
- All our contributors and supporters!

---

<p align="center">Made with ❤️ for the AI community</p>