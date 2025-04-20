---

# Face and Eye Detection with OpenCV

This project uses OpenCV's Haar cascade classifiers to perform real-time face and eye detection via webcam. It's built with C++ and managed using CMake.

## 🚀 Features

- Real-time face and eye detection using webcam input.
- Draws bounding circles or rectangles around detected faces.
- Detects eyes within detected face regions.
- Uses pre-trained Haar cascades provided by OpenCV.

## 📋 Requirements

- CMake ≥ 3.10
- OpenCV (built with the `opencv_contrib` data for access to Haar cascades)
- C++ compiler (e.g., g++, clang++, MSVC)

## 📂 Project Structure

```
.
├── CMakeLists.txt
├── main.cpp
└── README.md
```

## 🛠️ Build & Run

### 1. Clone the repository

```bash
git clone https://github.com/kanyutu707/facedetection.git
cd facedetection
```

### 2. Build with CMake

```bash
mkdir build
cd build
cmake ..
make
```

### 3. Run the program

```bash
./facedetection
```

## 🧠 How It Works

1. Loads Haar cascade XML files for:
   - Face: `haarcascade_frontalcatface.xml`
   - Eyes: `haarcascade_eye_tree_eyeglasses.xml`

2. Captures video from your default webcam.

3. Converts each frame to grayscale and resizes it.

4. Applies histogram equalization for better contrast.

5. Detects faces and eyes, then draws shapes to highlight them.

## 📁 Cascade File Locations

Make sure the Haar cascade files exist in OpenCV's sample data folder. The code uses:

```cpp
samples::findFile("haarcascades/haarcascade_frontalcatface.xml")
samples::findFile("haarcascades/haarcascade_eye_tree_eyeglasses.xml")
```

If you encounter issues loading these files, update the paths accordingly or ensure OpenCV was built with data support.

## ⌨️ Controls

- Press `q` or `Q` or `ESC` to exit the application.

## 📸 Sample Output

On successful detection, you’ll see bounding shapes drawn over faces and eyes in a display window titled **"Face Detection"**.

## 🧩 Acknowledgements

- Built with [OpenCV](https://opencv.org/)
- Uses Haar cascades from [OpenCV GitHub repository](https://github.com/opencv/opencv)

---
