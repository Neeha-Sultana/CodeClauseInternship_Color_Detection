# Color_Detection_CodeClause
This project is a Python program that allows users to detect and identify the color of a pixel in an image by double-clicking on it. It displays the color's name and its corresponding RGB values using OpenCV and a CSV color dataset.

Here's a breakdown of the color detection project point by point:

1. **Input Image Selection:** Users are prompted to enter the name of an image file they want to analyze.

2. **Library Imports:** The project imports two essential libraries:
   - `cv2` (OpenCV): Used for image processing.
   - `pandas`: Utilized for data management, particularly for reading a CSV file.

3. **CSV Color Dataset:** A CSV file named "colors.csv" is read into a Pandas DataFrame. This file contains information about various colors, including their names, hexadecimal values, and RGB components.

4. **Color Identification Function (`id_col_name`):** This function accepts RGB values (Red, Green, Blue) of a pixel as input. It calculates the minimum distance between the input RGB values and the values in the CSV dataset to identify the closest color match. It returns the name of the matched color.

5. **Mouse Double-Click Event Handling (`draw_func`):** A function is defined to handle mouse events, specifically detecting double-click events. When a user double-clicks on an image pixel, this function captures the RGB values of that pixel and stores them in global variables for further processing.

6. **Main Loop:** The program enters a while loop, continuously displaying the image using OpenCV's `imshow` function.

7. **Color Display:** Upon a double-click event, the program captures the RGB values of the selected pixel and displays a rectangle filled with the selected color on the image.

8. **Text Display:** The program generates a text string that includes the detected color name and the RGB values of the selected pixel.

9. **Text Color Adjustment:** If the sum of the RGB values of the detected color is high (indicating a very light color), the text is displayed in black to ensure visibility.

10. **User Interaction:** The program continues running until the user presses the 'Esc' key. It periodically checks for this key press using `cv2.waitKey`. When the user presses 'Esc,' the program breaks out of the loop.

11. **Cleanup:** Finally, the OpenCV windows are closed using `cv2.destroyAllWindows()`.

This project provides an interactive way for users to identify and inspect colors within an image, making it a useful tool for various design and image analysis applications.
