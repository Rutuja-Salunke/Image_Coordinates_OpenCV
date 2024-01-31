

### Project Overview:

**Objective:**
The project aims to create an interactive image viewer using the OpenCV library in Python. The viewer allows users to click on specific points within an image, providing real-time feedback on the coordinates of the clicked points and, in the case of right-clicks, the RGB color values at those points.

### Script Components:

1. **Importing Libraries:**
   - The script begins by importing the `cv2` module, which is the Python binding for OpenCV.

2. **Defining `click_event` Function:**
   - The `click_event` function is designed to handle mouse click events. It takes five parameters: `event`, `x`, `y`, `flags`, and `params`.
   - For left mouse clicks (`cv2.EVENT_LBUTTONDOWN`), it prints the coordinates to the console and displays them on the image.
   - For right mouse clicks (`cv2.EVENT_RBUTTONDOWN`), it prints both the coordinates and the RGB values of the clicked point to the console. These values are also displayed on the image.

3. **Handling Left Mouse Clicks:**
   - Upon a left mouse click, the script prints the coordinates to the console and overlays them on the image using `cv2.putText`.

4. **Handling Right Mouse Clicks:**
   - Upon a right mouse click, in addition to the coordinates, the script extracts the RGB values (B, G, R) of the clicked point and displays them alongside the coordinates on the image.

5. **Main Block (`__main__`):**
   - The script enters the main block, where the primary operations are performed.
   - It reads an image file using `cv2.imread` and stores it in the variable `img`.
   - The image is displayed using `cv2.imshow` with the window named according to the specified file path.
   - The mouse callback function is set to `click_event` using `cv2.setMouseCallback`. This means that the `click_event` function will be invoked whenever a mouse event occurs on the image window.
   - The script waits for a key press using `cv2.waitKey(0)` to keep the program open until a key is pressed.
   - Finally, it closes all open windows using `cv2.destroyAllWindows()`.

### Usage Instructions:

1. **Run the Script:**
   - Execute the script, and it will read and display an image.

2. **Interact with the Image:**
   - Left-click on the image to see the coordinates and see them displayed on the image.
   - Right-click to get both the coordinates and the RGB values, which are also displayed on the image.

3. **Close the Program:**
   - Press any key to close the program and the image window.

### Significance:

This script provides a simple yet effective tool for interactively exploring images. It enhances the understanding of pixel locations and color information within the image. The real-time display of coordinates and RGB values on the image window makes it a practical utility for visual inspection and analysis of images. The OpenCV library, with its versatile image processing capabilities, serves as a powerful foundation for such interactive applications.
