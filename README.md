# Web-based Plagiarism Checker

A modern, browser-based application for detecting similarities between text documents and source code files. Built with React, TypeScript, and Tailwind CSS, this tool provides real-time analysis of document similarities using advanced algorithms.

## Features

- **Multiple File Support**: Upload and compare multiple text or code files simultaneously
- **Advanced Text Processing**:
  - Case-insensitive comparison
  - Whitespace normalization
  - Punctuation removal
  - Code comment removal
- **Dual Algorithm Support**:
  - Cosine Similarity
  - Jaccard Index
- **Real-time Analysis**: Instant similarity scoring and phrase matching
- **Interactive UI**: Clean, responsive interface with drag-and-drop support
- **Detailed Reports**: Similarity percentages and common phrase detection

## Technology Stack

- React 18
- TypeScript
- Tailwind CSS
- Vite
- Lucide React Icons

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/kyk29718/Plagiarism-Checker.git
```

2. Install dependencies:
```bash
cd plagiarism-checker
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:5173`

## Usage

1. Upload files using the file upload button or drag-and-drop
2. Configure preprocessing options:
   - Ignore case
   - Remove whitespace
   - Remove punctuation
   - Remove code comments
3. Select similarity algorithm (Cosine or Jaccard)
4. Click "Run Plagiarism Check"
5. View results in the right panel

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details

## Potential Interview Questions

### Technical Questions

1. **Algorithm Implementation**
   - Q: "Explain how the Cosine Similarity algorithm works in your implementation."
   - A: The implementation converts text into word frequency vectors, calculates the dot product between vectors, and divides by the product of their magnitudes. This measures the cosine of the angle between vectors, providing a similarity score between 0 and 1.

2. **React Performance**
   - Q: "How did you optimize the performance of the file processing system?"
   - A: The implementation uses useCallback for memoization of functions, processes files in batches using setTimeout to prevent UI freezing, and implements efficient state management for file handling.

3. **State Management**
   - Q: "Why did you choose React's useState over other state management solutions?"
   - A: For this application, component-level state management was sufficient as the state is contained within a single component tree. useState provides clean, simple state management without the overhead of external libraries.

4. **TypeScript Integration**
   - Q: "How does TypeScript improve the reliability of your code?"
   - A: TypeScript provides type safety for file data structures, comparison results, and preprocessing options. This catches potential errors at compile-time and improves code maintainability.

### System Design Questions

1. **Scalability**
   - Q: "How would you modify the system to handle very large files?"
   - A: Implement file streaming, chunk processing, and Web Workers for background processing. Add progress indicators and cancel capabilities for long-running comparisons.

2. **Architecture Decisions**
   - Q: "Why choose a client-side approach over server-side processing?"
   - A: Client-side processing eliminates server costs, provides instant feedback, and ensures privacy as files never leave the user's browser. It also reduces infrastructure complexity.

3. **Feature Extension**
   - Q: "How would you add support for comparing programming language syntax?"
   - A: Implement language-specific tokenizers, abstract syntax tree comparison, and specialized preprocessing for different programming languages.

### Problem-Solving Questions

1. **Edge Cases**
   - Q: "How does your system handle files with different encodings?"
   - A: The FileReader API handles various text encodings. Additional preprocessing steps could be added to normalize character encodings before comparison.

2. **Algorithm Selection**
   - Q: "Why offer both Cosine and Jaccard similarity metrics?"
   - A: Different metrics suit different use cases. Cosine similarity works better for frequency-based comparison, while Jaccard is better for set-based comparison of unique terms.

3. **User Experience**
   - Q: "How do you handle failed file uploads or processing errors?"
   - A: The system implements error boundaries, provides user feedback through the UI, and includes fallback mechanisms for failed operations.

These questions cover various aspects of the application, from technical implementation details to system design decisions and problem-solving approaches.
