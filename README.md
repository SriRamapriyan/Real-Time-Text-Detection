# Python-OpenCV Text Detection  

This project uses OpenCV to detect text in real-time through a video stream. The EAST (Efficient and Accurate Scene Text) text detection model is used to identify and highlight text in the camera's video feed.  

## Features  
- Real-time text detection from a live camera feed.  
- Uses the pre-trained EAST text detection model for accurate results.  
- Highlights and extracts text regions from the video feed.  

## Prerequisites  

Make sure you have the following installed:  
1. Python 3.7 or later  
2. OpenCV 4.5 or later  
3. NumPy  

To install the required dependencies, run:  
```bash  
pip install opencv-python-headless numpy  
```  

## Files  

- **`main.py`**: The main script for running the text detection.  
- **`frozen_east_text_detection.pb`**: The pre-trained EAST model file.  

## Usage  

1. Clone the repository:  
   ```bash  
   git clone https://github.com/your-repo/python-opencv-text-detection.git  
   cd python-opencv-text-detection  
   ```  

2. Ensure the `frozen_east_text_detection.pb` file is in the same directory as `main.py`.  

3. Run the program:  
   ```bash  
   python main.py --east frozen_east_text_detection.pb  
   ```  

4. The camera stream will open. Any text brought into the frame will be detected and highlighted.  

## Command-Line Arguments  

- `--east`: Path to the frozen EAST text detection model file (required).  
- `--width`: (Optional) Set the width of the input frame. Default is 320.  
- `--height`: (Optional) Set the height of the input frame. Default is 320.  

Example with custom frame dimensions:  
```bash  
python main.py --east frozen_east_text_detection.pb --width 640 --height 480  
```  

## Output  

- The detected text regions are highlighted in the video feed.  
- Optionally, you can modify the script to save the detected text regions to a file.  

## Troubleshooting  

- **No camera detected**: Ensure your webcam is connected and accessible.  
- **Low detection accuracy**: Experiment with frame dimensions or preprocess the video feed for better results.  

## Acknowledgments  

- EAST Model: Pre-trained model for Efficient and Accurate Scene Text Detection.  
- OpenCV: Open-source computer vision and machine learning library.  
