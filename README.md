# Cryptography
Title: Data shielding using Steganography

Idea: The file to be secured is embedded in an image without distorting it.

Approach:
A) Embedding:
1) The vessel image is loaded in memory as a 2D array of pixels.
2) An embedding header is created so that extraction becomes possible.
3) The file to be secured is read byte by byte.
4) Each byte is broken into bit set (3+3+2) and embedded into a band of the pixel using LSB technique.
6) The 2D array of pixels is save back as image (with embedding). 

B) Extraction:
1) The image with embedding is loaded in memory as a 2D array of pixels.
2) The header is fetched to know the type and quantity of embedding.
3) The bands of pixels of the array are read to extract bits at LSB.
4) The read bits are clubbed to form the bytes back.
6) The bytes are written to form the file that was shielded inside the image.

Language: Python
Extrenal Libraries: OpenCV
