# Huffman Coding Implementation for Text Files in C++

## Introduction

This project implements Huffman Coding, a lossless data compression algorithm in C++. Huffman Coding is a widely-used technique in information theory for compressing data without losing any information. This project can compress and decompress text files, showcasing the practical application of this algorithm.

## Features

- **Encode**: Compress any text file into a `.huf` file using Huffman Coding, significantly reducing file size while preserving data integrity.
- **Decode**: Decompress a Huffman-coded `.huf` file back to its original text file format.
- **Efficient Compression**: The project uses advanced data structures like Min Heap and Huffman Tree to optimize the compression process.
- **Custom Implementation**: The project includes custom implementations of key components, such as creating the Huffman tree, generating binary codes, and handling file input/output.

## How It Works

### Compression (Encoding)

1. **createMinHeap()**: Reads the input file and calculates the frequency of each character. These characters and their frequencies are stored in a Min Heap structure using a priority queue.
  
2. **createTree()**: Constructs the Huffman Tree by repeatedly extracting nodes with the lowest frequencies from the Min Heap, combining them into a new node, and inserting this node back into the heap. This process continues until a single node remains.

3. **createCodes()**: Traverses the Huffman Tree to generate binary Huffman codes for each character based on their position in the tree.

4. **saveEncodedFile()**: Saves the encoded data into an output file with a `.huf` extension. The file includes both the Huffman codes and the encoded content of the original text file.

### Decompression (Decoding)

1. **getTree()**: Reconstructs the Huffman Tree from the Min Heap data stored in the `.huf` file, allowing the original character codes to be restored.

2. **saveDecodedFile()**: Converts the binary codes in the encoded file back into their corresponding characters by traversing the reconstructed Huffman Tree. The decoded content is saved into the original text file format.

## Example

An example of the compression and decompression process:

- **Input File**: `inputFile.txt` (2.2MB)
- **Compressed File**: `compressedFile.huf` (1.1MB)
- **Decompressed File**: `outputFile.txt` (2.2MB)

This example demonstrates the effectiveness of Huffman Coding in reducing file size while allowing for full recovery of the original content.

## How to Run

### Prerequisites

- A C++ compiler (e.g., GCC, Clang)
- Basic understanding of C++ programming

### Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/ppsingh21/HuffmanCoding.git
2. **Compile the Code:**
   ```bash
   g++ -o huffman huffman.cpp
3. **Run Compression:**
   ```bash
   ./huffman encode inputFile.txt compressedFile.huf
4. **Run Decompression:**
   ```bash
   ./huffman decode compressedFile.huf outputFile.txt

## Limitations

This implementation serves as an educational example of Huffman Coding and may not be as optimized as modern compression tools.
The efficiency of the algorithm can vary depending on the nature of the input text files.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For any questions or suggestions, feel free to reach out:

GitHub: [ppsingh21](https://github.com/ppsingh21)
