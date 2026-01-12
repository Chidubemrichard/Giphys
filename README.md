Giphys.py
📌 Overview
Giphys.py is a simple Python script that converts multiple images into an animated GIF.
This personal project uses the imageio library to read image files and combine them into a looping GIF animation.

The script is beginner-friendly and designed so users can easily modify the image filenames to include more frames.

🛠 Requirements
Python 3.11
imageio
pillow
Install the required libraries using:

bash
pip install imageio pillow
📂 Project Structure
text
Gif projects/
│
├── Giphys.py
├── team-pic1.png
├── team-pic2.png
└── team.gif   (generated output)
▶️ How to Run
Navigate to the project directory and run:

bash
python3 Giphys.py
Once executed, the script will generate an animated GIF in the same directory.

🧠 How It Works
Image filenames are stored in a list.
Each image is read into memory using imageio.
The images are written into a single animated GIF.
The GIF loops indefinitely with a fixed duration between frames.
🧩 Example Code
python
import imageio.v3 as iio

filenames = ['team-pic1.png', 'team-pic2.png']
images = []

for filename in filenames:
    images.append(iio.imread(filename))

iio.imwrite(
    'team.gif',
    images,
    duration=500,
    loop=0
)
🖼 Customizing Images
To add or change images, update the filenames list:

python
filenames = [
    'image1.png',
    'image2.png',
    'image3.png'
]
✅ All images should be the same dimensions for best results.

⏱ GIF Settings
duration: Time each frame is shown (in milliseconds)
loop:
0 → infinite loop
1 → plays once
Example:

python
duration=300
⚠️ Common Issues
Wrong File Extension
Make sure the output file ends in .gif:

python
iio.imwrite('team.gif', images)
Using an incorrect extension (e.g., .gfif) will cause an error.

Missing Libraries
If you see a backend error, ensure Pillow is installed:

bash
pip install pillow
🚀 Future Improvements (Ideas)
Automatically load all images from a folder
Add command-line arguments
Resize images automatically
Control FPS instead of duration
📜 License
This project is a personal project and is currently not licensed for redistribution.