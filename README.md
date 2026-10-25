# Image-Handling-and-Pixel-Transformations-Using-OpenCV 

## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image.  
2) Adjust the brightness of an image.  
3) Modify the image contrast.  
4) Generate a third image using bitwise operations.

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:
### Step 1:
Load an image from your local directory and display it.

### Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

### Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.  
Display the original, brighter, and darker images.

### Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).  
Display the original, lower contrast, and higher contrast images.

### Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
 ## Name:SAFIRA BARVEEN S
 ## Register Number:212224230235

  ## Ex. No. 01
```
import cv2
import matplotlib.pyplot as plt
```
```python
# Read the image using OpenCV
img = cv2.imread('photo.jpeg', cv2.IMREAD_COLOR)
```
```python
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

```python
# Display the image using matplotlib imshow().
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```
## OUTPUT :

<img width="1136" height="540" alt="Screenshot 2026-10-25 210747" src="https://github.com/user-attachments/assets/e6c1e57d-32b7-4d6d-bee5-b0ea710366c8" />



```python
# Load the image
image = cv2.imread('photo.jpeg') 
```
```python
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
```

<img width="244" height="43" alt="image" src="https://github.com/user-attachments/assets/d25ddf8f-aba8-498f-9fab-6e8c3245e94c" />

```python
# Draw a line from top-left to bottom-right
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)
```
```python
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```

## OUTPUT :

<img width="1182" height="502" alt="Screenshot 2026-10-25 211249" src="https://github.com/user-attachments/assets/292b37d5-969a-458a-9b30-d201186e7ac6" />


```python
# Load the image
image = cv2.imread('photo.jpeg')

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape

```
## OUTPUT :

<img width="1182" height="502" alt="Screenshot 2026-10-25 211249" src="https://github.com/user-attachments/assets/31d59488-1335-4eb1-b6ca-045d0a9c234e" />


```
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)
```

```python
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```

## OUTPUT :

<img width="1142" height="487" alt="Screenshot 2026-10-25 211257" src="https://github.com/user-attachments/assets/4d5f93f7-296c-46de-be51-0c5cae619e00" />



```
# Load the image
image = cv2.imread('photo.jpeg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img.shape
```

<img width="233" height="42" alt="image" src="https://github.com/user-attachments/assets/4e124fc0-a314-4e0d-8b77-814ce105e62f" />

```python
# Draw a rectangle around the Whole image
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)
```
```python
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

## OUTPUT :
<img width="1107" height="485" alt="Screenshot 2026-10-25 211303" src="https://github.com/user-attachments/assets/e1dfa290-7034-45be-84e2-c18360942656" />



```
# Load the image
image = cv2.imread('photo.jpeg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
```
# Add text to the image
text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
```
```
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```

## OUTPUT :

<img width="1092" height="495" alt="Screenshot 2026-10-25 211309" src="https://github.com/user-attachments/assets/5fd6ec77-cc40-458a-a0f5-eafbd7802da3" />



```python
# Load the image
image = cv2.imread('photo.jpeg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```
```python
# Original RGB Image
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```
## OUTPUT : 

<img width="1116" height="505" alt="Screenshot 2026-10-25 211316" src="https://github.com/user-attachments/assets/28f44170-8f48-4d42-af82-2caa935b0d7c" />

```python
# Convert RGB to HSV
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)

# HSV Image
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```

# OUTPUT :

<img width="1086" height="505" alt="Screenshot 2026-10-25 211322" src="https://github.com/user-attachments/assets/edef8f25-1bc8-4285-a886-afbbf34b5e82" />



```python
# Convert RGB to GRAY
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
```
```python
# Grayscale Image
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```

## OUTPUT :

<img width="1101" height="510" alt="Screenshot 2026-10-25 211329" src="https://github.com/user-attachments/assets/758346ef-3f29-4a42-9c85-48866d3f7e30" />


```python
# Convert RGB to YCrCb
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
```
```
# YCrCb Image
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
```

## OUTPUT :

<img width="1031" height="480" alt="Screenshot 2026-10-25 211335" src="https://github.com/user-attachments/assets/3ed1fcb0-63ff-488f-8e62-32f79cd7744b" />



```python
# Convert HSV back to RGB
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```

## OUTPUT :

<img width="1100" height="495" alt="Screenshot 2026-10-25 211341" src="https://github.com/user-attachments/assets/e9efad0c-e3c1-4056-9665-7dd9a8a72330" />


```python
# Modify a block of pixels (300x300) to white, starting from (200, 200)
image[200:500, 200:500] = [255, 255, 255]  # Rows: 200-499, Columns: 200-499

# Convert BGR to RGB for displaying with Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```
```
# Display the modified image
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```

## OUTPUT :

<img width="1167" height="495" alt="Screenshot 2026-10-25 211347" src="https://github.com/user-attachments/assets/77d3e9fe-da7e-4ceb-b0ca-09e1d58cded7" />


```
# Load the image
image = cv2.imread('photo.jpeg')
image.shape
```
<img width="183" height="44" alt="image" src="https://github.com/user-attachments/assets/877e33d2-5758-43bb-b338-d7e2933874ec" />

```
# Resize the image to half its size
resized_image = cv2.resize(image, (768 // 2, 600 // 2))  # (new_width, new_height)

# Convert BGR to RGB for displaying with Matplotlib
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
```

<img width="199" height="44" alt="image" src="https://github.com/user-attachments/assets/ae8f2ba6-05c1-44e6-83e4-b274aac15330" />

```
# Display the resized image
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```

## OUTPUT :

<img width="1082" height="500" alt="Screenshot 2026-10-25 211355" src="https://github.com/user-attachments/assets/cf0c18a4-21a8-4baf-acb4-6b34a927928e" />



```
# Load the image
image = cv2.imread('photo.jpeg')
image.shape
```
<img width="204" height="48" alt="image" src="https://github.com/user-attachments/assets/e9d9fcba-6eaa-428d-813b-581e412d6358" />

```
# Crop a 300x300 region starting from (50, 50)
roi = image[50:350, 50:350]  # Rows: 50-349, Columns: 50-349

# Convert BGR to RGB for displaying with Matplotlib
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
```
```
# Display the cropped region (ROI)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```
## OUTPUT :

<img width="1061" height="522" alt="Screenshot 2026-10-25 211402" src="https://github.com/user-attachments/assets/8ca6419b-fa3a-4510-b6ac-21399765cd6c" />


```
# Load the image
image = cv2.imread('photo.jpeg')

# Flip the image horizontally (left-right)
flipped_horizontally = cv2.flip(image, 1)

# Convert BGR to RGB for displaying with Matplotlib
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
```
```
# Horizontal flip
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```
## OUTPUT :

<img width="1020" height="517" alt="Screenshot 2026-10-25 211408" src="https://github.com/user-attachments/assets/a87c909e-4696-4c4f-8d42-13d211e7bb19" />



```
# Flip the image vertically (up-down)
flipped_vertically = cv2.flip(image, 0)

# Convert BGR to RGB for displaying with Matplotlib
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
```
```
# Vertical flip
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```
## OUTPUT :

<img width="1036" height="496" alt="Screenshot 2026-10-25 211415" src="https://github.com/user-attachments/assets/f4c04103-f1eb-41ef-929b-cd63f613354f" />



## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.

