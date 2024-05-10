# Compress-Files-using-Huffman-encryption-algorithm
a c++ program used to compress files using the huffman encryption algorithm.

Huffman Tree Construction:
The program reads an input binary file (astro.bmp) and determines the frequency of each character (or byte) in the file.
It then constructs a Huffman tree based on these frequencies. In a Huffman tree, characters with higher frequencies are placed closer to the root, while those with lower frequencies are placed further away.

Encoding:
Once the Huffman tree is constructed, each character in the file is assigned a unique binary code based on its position in the tree. These codes are shorter for characters that appear more frequently and longer for characters that appear less frequently.
The program translates the Huffman tree into a set of binary codes for each character, which will be used for compression.

Compression:
With the Huffman codes determined, the program compresses the original file by replacing each character with its corresponding Huffman code.
The compressed data is written to a new binary file (astrocomp.bmp), which contains a more compact representation of the original data.

Decompression:
To decompress the data, the program reads the compressed binary file (astrocomp.bmp).
It then traverses the Huffman tree in reverse, using the Huffman codes to reconstruct the original characters.
The decompressed data is written to another binary file (astro2.bmp), which should be identical to the original input file (astro.bmp).

Cleanup and Output:
Finally, the program outputs statistics such as the total number of characters in the original file and the decompressed file.
It also handles memory deallocation and closes any open files before exiting.
Overall, this program demonstrates how Huffman coding can be used to efficiently compress and decompress data while preserving its original content.
