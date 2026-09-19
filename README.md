This project reduces the color complexity of an image from millions of 
colors to a specific palette (e.g., 16 colors) using Unsupervised Machine 
Learning.
1. Environment Setup :
Install the required Python libraries using pip:
pip install numpy matplotlib scikit-learn pillow
2. Input Phase :
• Load Image: Use PIL (Pillow) to open the source image 
(img.jpg).
• Normalize: Convert pixel values from a 0-255 range to a 0-1 range 
(float64) to help the algorithm converge faster.
3. Pre-Processing :
• Flattening: A standard image is a 3D array (Height, Width, RGB). 
We reshape it into a 2D array (Pixels, RGB) so each pixel is treated 
as a single data point in a 3D color space.
4. The K-Means Algorithm :
• Initialize: Set $K=16$ (the number of final colors desired).
• Fit: The algorithm identifies 16 "centroids" (average colors) that 
best represent all pixels in the image.
• Predict: Every pixel in the image is assigned the label of its nearest 
centroid.
5. Stylization & Color Mapping :
• Before (Grayscale): The original centroids represent shades of gray.
• After (Colorized): We manually replace the gray centroids with a 
curated palette (e.g., Deep Blues and Sky Blues) to transform the 
abstract pattern into a stylized digital asset.
6. Output Phase :
• Reconstruct: Reshape the flattened pixel list back into the original 
(Height, Width, RGB) dimensions.
• Comparison: Use matplotlib to display the "Before" (Original) 
and "After" (Compressed/Colorized) images side-by-side.
• Save: Export the final result as a high-quality PNG or JPG
