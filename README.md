# File Compression Tool

A web-based file compression and decompression tool using Huffman Coding algorithm. Built with Flask and featuring an interactive animated UI powered by Vanta.js.

## 📋 Overview

This project implements a lossless file compression system using the Huffman Coding algorithm. Users can upload text files to compress them into binary format or decompress previously compressed files back to their original form through an elegant web interface.

## ✨ Features

- **Huffman Coding Algorithm**: Efficient lossless compression using frequency-based encoding
- **Compress Files**: Upload any text-based file and compress it to reduce file size
- **Decompress Files**: Restore compressed binary files to their original text format
- **Interactive UI**: Animated backgrounds using Vanta.js with Three.js
- **Instant Download**: Automatically download compressed/decompressed files
- **User-Friendly Interface**: Clean, modern design with smooth animations and transitions
- **Real-time Feedback**: Visual alerts for successful operations or errors

## 🛠️ Technologies Used

### Backend
- **Flask**: Python web framework
- **Python 3**: Core programming language
- **Huffman Algorithm**: Custom implementation for compression/decompression

### Frontend
- **HTML5/CSS3**: Structure and styling
- **JavaScript/jQuery**: Interactive functionality
- **Vanta.js**: Animated background effects
- **Three.js**: 3D graphics library
- **Bootstrap 3**: UI components and alerts

## 🧮 How Huffman Coding Works

Huffman Coding is a lossless data compression algorithm that:

1. **Analyzes Frequency**: Counts the occurrence of each character in the text
2. **Builds Binary Tree**: Creates a binary tree based on character frequencies
3. **Generates Codes**: Assigns shorter binary codes to more frequent characters
4. **Encodes Data**: Replaces characters with their binary codes
5. **Stores Tree**: Saves the Huffman tree for decompression

This results in significant file size reduction for text files!

## 🚀 Installation & Setup

### Prerequisites

- Python 3.7 or higher
- pip (Python package manager)

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/file-compression-tool.git
cd file-compression-tool
```

### Step 2: Install Dependencies

```bash
pip install flask
```

### Step 3: Run the Application

```bash
python app.py
```

The application will start on `http://127.0.0.1:5000/`

## 📁 Project Structure

```
file-compression-tool/
│
├── app.py                  # Main Flask application
├── huffman.py             # Huffman coding implementation
├── README.md              # Project documentation
│
├── templates/             # HTML templates
│   ├── home.html         # Landing page
│   ├── compress.html     # Compression page
│   └── decompress.html   # Decompression page
│
└── uploads/              # Temporary storage for uploaded files
    └── (uploaded files stored here temporarily)
```

## 💻 Usage

### Compressing a File

1. Navigate to `http://127.0.0.1:5000/` in your web browser
2. Click the **COMPRESS** button
3. Select a text-based file (e.g., .txt, .csv, .log)
4. Click **Upload** and wait for processing
5. The compressed `.bin` file will automatically download

### Decompressing a File

1. From the home page, click the **DECOMPRESS** button
2. Select a previously compressed `.bin` file
3. Click **Upload** and wait for processing
4. The decompressed `.txt` file will automatically download

## 📊 File Format

### Compressed File Structure

The compressed `.bin` file contains:
1. **Header**: Huffman tree codes (character-to-binary mapping)
2. **Body**: Encoded binary data

This structure allows the decompression algorithm to rebuild the original text.

## 🎨 UI Features

- **Home Page**: Purple animated network background with NET effect
- **Compress Page**: Red animated dots background with DOTS effect
- **Decompress Page**: Blue animated dots background with DOTS effect
- **Hover Effects**: Buttons transform on hover for better UX
- **Success Alerts**: Green alerts for successful operations
- **Error Alerts**: Red alerts for failed operations

## ⚙️ Key Components

### huffman.py

Contains the core compression logic:
- `Node`: Binary tree node class for Huffman tree
- `build_tree()`: Constructs Huffman tree from character frequencies
- `build_codes()`: Generates binary codes for each character
- `compress()`: Compresses input file and saves as binary
- `decompress()`: Restores original file from compressed binary

### app.py

Flask application with routes:
- `/`: Home page
- `/compress`: Compression interface (GET) and processing (POST)
- `/decompress`: Decompression interface (GET) and processing (POST)

## 📈 Compression Efficiency

Huffman Coding typically achieves:
- **20-90% compression** depending on text redundancy
- **Better results** for texts with repeated patterns
- **Lossless compression** - no data loss during compression/decompression

## ⚠️ Important Notes

- **Text Files Only**: This tool is designed for text-based files
- **Binary Files**: Images, videos, and executables are not supported
- **Temporary Storage**: Uploaded files are stored in the `uploads/` folder
- **File Cleanup**: Consider implementing automatic cleanup for the uploads folder

## 🔒 Security Considerations

For production deployment, consider:
- Implementing file size limits
- Adding file type validation
- Sanitizing uploaded filenames
- Securing the uploads directory
- Adding user authentication
- Implementing rate limiting

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🐛 Known Issues

- Large files may take longer to process
- The `uploads/` folder can accumulate files over time
- No file size limit implemented by default

## 🔮 Future Enhancements

- Add support for multiple file compression (ZIP-like functionality)
- Implement compression ratio statistics
- Add file size comparison (before/after)
- Create progress indicators for large files
- Add drag-and-drop file upload
- Implement automatic cleanup of temporary files
- Add compression level options

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

Aashish Joshi - [AAs6395](https://github.com/AAs6395)

## 🙏 Acknowledgments

- Huffman Coding algorithm by David A. Huffman
- Vanta.js for amazing background animations
- Flask framework and community
- Bootstrap for UI components

---

**Note**: This tool is for educational purposes. For production use, consider additional features like error handling, file validation, and security measures.
