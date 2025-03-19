# ImageMagic: Transform Your World of Pixels

## Introduction
Welcome to **ImageMagic**, an innovative project designed to explore image manipulation through the power of linked lists. ImageMagic enables you to break down an image into distinct segments, store them in a unique linked list structure (Chain), and apply a variety of transformations. This project allows you to unleash your creativity and dive into the fascinating world of digital image processing.

## Features
### **Block Manipulation (`block.h`)**
The **Block** class enables you to segment an image into blocks and manipulate them with various transformations. Key functionalities include:
- Extracting and positioning blocks within an image canvas.
- Performing operations such as rendering, horizontal flipping, and 90-degree counter-clockwise rotation.

### **Chain Processing (`chain.h`)**
The **Chain** class serves as the core linked list structure that organizes blocks into a sequence. This structure provides powerful operations such as:
- Reversing the sequence of blocks.
- Flipping the entire chain horizontally.
- Rotating all blocks 90 degrees counter-clockwise.

### **Rendering (`chain.h`)**
ImageMagic allows you to render a chain of manipulated blocks into a cohesive output image. Using the `Render` function, you can generate a final image by specifying the number of columns to arrange the blocks.

## Getting Started
To begin using ImageMagic, follow these steps:

1. Ensure you have a C++ development environment set up.
2. Clone or download the repository.
3. Explore the project structure and review the documentation.
4. Build the project using the provided build instructions.
5. Run the executable, specifying an input image and desired block dimensions.

## Usage
### **Block Manipulation**
Utilize the **Block** class to segment an image and apply transformations such as:
- Flipping horizontally
- Rotating counter-clockwise
- Rendering individual blocks onto a canvas

### **Chain Operations**
With the **Chain** class, you can:
- Create a linked sequence of image blocks
- Apply transformations across the entire chain
- Generate a final output image

### **Rendering the Final Image**
Once your chain is fully processed, use the `Render` function to generate the final image, specifying the number of columns for block arrangement.

## Example Usage
```cpp
#include "block.h"
#include "chain.h"

int main() {
    // Load an input image
    PNG inputImage;
    inputImage.readFromFile("input.png");

    // Define block size
    unsigned int blockSize = 10;

    // Create a chain of blocks from the input image
    Chain imageChain(inputImage, blockSize);

    // Flip the chain horizontally
    imageChain.FlipHorizontal(inputImage.width());

    // Rotate the chain counter-clockwise
    imageChain.RotateCCW(inputImage.width());

    // Render the chain into a single output image with 5 columns
    PNG outputImage = imageChain.Render(5);

    // Save the output image
    outputImage.writeToFile("output.png");
    
    return 0;
}
```

## Contributing
Contributions are welcome! If you discover bugs, have feature suggestions, or want to improve ImageMagic, feel free to open an issue or submit a pull request.

## License
ImageMagic is licensed under the **MIT License**. For more details, refer to the `LICENSE` file.

## Acknowledgments
ImageMagic draws inspiration from the world of digital image processing and creative coding. Special thanks to the developer community for their contributions to C++ and linked list-based data structures. Happy coding!

---

