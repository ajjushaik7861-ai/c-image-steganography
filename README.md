Image Steganography in C

A C-based image steganography project that hides secret text inside BMP images using the Least Significant Bit (LSB) technique and retrieves it without degrading image quality.

📌 Project Description

This project demonstrates secure data hiding using low-level file handling and bit manipulation in C.
Secret text data is embedded into a BMP image during encoding and extracted back during decoding.

🛠️ Technologies Used

Language: C

Compiler: GCC

Concepts:

File I/O

Bitwise operations

BMP image structure

LSB steganography

📂 Project Structure
image-steganography-c/
│── main.c
│── encode.c
│── encode.h
│── decode.c
│── decode.h
│── common.h
│── types.h
│── secret.txt
│── beautiful.bmp
│── output.bmp
│── output.txt

📁 File-wise Explanation
🔹 Source Files (.c)
main.c

Entry point of the program

Handles command-line arguments

Decides whether to encode (-e) or decode (-d)

Calls appropriate functions from encode or decode modules

encode.c

Implements the encoding logic

Reads the secret text file

Embeds text data into the BMP image using LSB

Writes the encoded image to output.bmp

decode.c

Implements the decoding logic

Reads the encoded BMP image

Extracts hidden text from LSBs

Writes decoded message to output.txt

🔹 Header Files (.h)
encode.h

Function declarations related to encoding

Encoding-related structures and macros

decode.h

Function declarations related to decoding

Decoding-related data structures

common.h

Common macros and utility functions

Shared constants used by both encoder and decoder

types.h

Custom data types and enums

Improves code readability and maintainability

🔹 Text Files (.txt)
secret.txt

Contains the secret message to be hidden

Input file for the encoding process

output.txt

Stores the decoded secret message

Generated after successful decoding

🔹 Image Files (.bmp)
beautiful.bmp

Original BMP image

Used as input for encoding

output.bmp

Output image after encoding

Contains the hidden secret data

Looks visually identical to the original image

⚙️ Compilation

Compile all source files using GCC:

gcc main.c encode.c decode.c -o stego

▶️ Execution
🔐 Encoding (Hide Secret Text)
./stego -e beautiful.bmp secret.txt output.bmp

🔓 Decoding (Extract Secret Text)
./stego -d output.bmp output.txt

🔍 How LSB Steganography Works

BMP images store pixel data as bytes

The least significant bit of each byte is replaced with secret data

Changes are too small to be noticed by the human eye

Data is reconstructed during decoding

🚀 Future Enhancements

Encrypt secret message before embedding

Support PNG and JPEG formats

Password-based decoding

GUI-based application

👤 Author
MD Abdul Azeez
