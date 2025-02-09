# **Parking Space Detection using OpenCV**  

This project detects available parking spaces in a given video feed using **computer vision techniques** in OpenCV. It processes the video frame by frame, applies **image preprocessing**, and checks each parking space for occupancy based on pixel intensity.

---

## **Features**  
✅ Reads a **video file** and processes each frame.  
✅ Converts frames to **grayscale** and applies **Gaussian blur** for noise reduction.  
✅ Uses **adaptive thresholding** and **median blur** to highlight edges.  
✅ Applies **morphological dilation** to enhance the detected parking spots.  
✅ Checks each **predefined parking space** for vacancy based on pixel intensity.  
✅ Displays the **number of free parking spots** in real time.  

---

## **Installation**  

### **1. Clone the Repository**
```bash
git clone https://github.com/Muhammadfakharulhasnain/OpenCV_Project_Parking_Space_Counter.git
cd OpenCV_Project_Parking_Space_Counter
```

### **2. Install Dependencies**
Ensure you have Python installed, then run:
```bash
pip install opencv-python numpy
```

---

## **Usage**  
1. Place your **video file** inside the `image_video/` folder and update the script if necessary.  
2. Run the script:
```bash
python main.py
```
3. The program will process the video and display **real-time parking availability**.  
4. Press **'1'** to exit the program.  

---

## **Project Structure**  
```
/your-repository
│-- image_video/
│   ├── video.mp4              # Input video file
│-- carparkpos                 # Pickle file storing parking positions
│-- main.py                     # Main script for processing video
│-- positionfinder.py
│-- make_rectangle.py                   
│-- README.md                   # Project documentation
```

---

## **How It Works**  
🔹 **Load Parking Positions**: Reads `carparkpos` (predefined parking spot positions).  
🔹 **Preprocessing Video Frames**:  
   - Convert to **grayscale**  
   - Apply **Gaussian blur** to smooth noise  
   - Use **adaptive thresholding** to detect edges  
   - Apply **median blur** to remove small artifacts  
   - Perform **dilation** to enhance the edges  
🔹 **Check Parking Spaces**:  
   - Extract each **parking space** from the processed frame  
   - Count the **non-zero pixels** (white areas)  
   - If pixel count is **below 900**, mark as **free** (green), else **occupied** (red)  
🔹 **Display Results**: Draws rectangles around parking spots and shows available spaces.  

---

## **Example Output**  
🚗 **Red Rectangle** = Occupied  
🟩 **Green Rectangle** = Free  
🟢 **Top-left counter** = Number of free spots  



## **Future Improvements**  
✅ Improve accuracy using **deep learning models** (YOLO, CNNs).  
✅ Implement **real-time camera** support.  
✅ Add a **web-based dashboard** for remote monitoring.  

---

## **License**  
This project is open-source under the **MIT License**. Feel free to use, modify, and contribute! 
