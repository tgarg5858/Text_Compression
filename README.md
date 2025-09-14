
# Huffman Coding Compression Tool

This C++ project implements **Huffman Coding**, a lossless data compression algorithm. It reads input from a file, compresses the contents using Huffman encoding, writes the encoded data and the Huffman codes to separate files, and then decodes the data to verify the process.

---

## 📁 Files

* `main.cpp` — Source code (the file you've provided).
* `input.txt` — Input file containing the text to compress.
* `encoded.txt` — Output file containing the encoded binary string.
* `codes.txt` — Output file containing character-to-code mappings.
* `decoded.txt` — Output file containing the decoded (original) text.

---

## 🚀 Features

* Builds a **Huffman Tree** based on character frequencies.
* Generates **binary Huffman codes** for each character.
* Encodes the input text into a binary string.
* Decodes the encoded string to validate correctness.
* Saves encoded data and Huffman codes to external files.

---

## 🧠 How It Works

1. **Frequency Counting**:
   Each character’s frequency in the input file is counted.

2. **Building the Huffman Tree**:
   A min-heap is used to construct the Huffman Tree based on the frequency of characters.

3. **Generating Huffman Codes**:
   The tree is traversed to assign a unique binary code to each character.

4. **Encoding**:
   Each character in the original text is replaced with its Huffman code.

5. **Decoding**:
   The encoded binary string is decoded back using the Huffman tree.

---

## 🛠️ How to Compile and Run

### 🔧 Requirements

* C++ Compiler (e.g., g++)
* C++11 or above

### 📦 Compilation

```bash
g++ -std=c++11 -o huffman main.cpp
```

### ▶️ Running

1. Place your input text in a file named `input.txt` in the same directory.
2. Run the program:

```bash
./huffman
```

3. After execution, the following files will be generated:

   * `encoded.txt`: Compressed binary data.
   * `codes.txt`: Character to Huffman code mappings.
   * `decoded.txt`: Decoded text (should match `input.txt`).

---

## 📌 Example

If `input.txt` contains:

```
hello world
```

After running, `codes.txt` might look like:

```
h 1011
e 1010
l 00
o 01
' ' 111
w 1101
r 1100
d 100
```

`encoded.txt` will contain a binary string like:

```
101110100000010111101101100100
```

`decoded.txt` will contain:

```
hello world
```

---

## 📂 Output Files Explained

| File          | Description                         |
| ------------- | ----------------------------------- |
| `encoded.txt` | Binary-encoded version of the input |
| `codes.txt`   | Character-to-code mappings          |
| `decoded.txt` | Reconstructed original text         |

---

## ⚠️ Notes

* Special characters like newline (`\n`) and space (`' '`) are handled explicitly in `codes.txt`.
* This version uses in-memory structures. It is **not optimized for large file compression** or real binary file handling.
* Output in `encoded.txt` is stored as a string of `'0'` and `'1'` characters, not raw binary.

---

## 📄 License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT).

---

Let me know if you want me to auto-generate the `input.txt` or provide a version that handles raw binary I/O for better compression.
