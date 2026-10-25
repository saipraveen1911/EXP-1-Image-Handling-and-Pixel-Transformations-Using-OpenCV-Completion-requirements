# EXP-1-Image-Handling-and-Pixel-Transformations-Using-OpenCV

## Developed by : SAI PRAVEEN C

## REGISTER NUMBER : 212225230239

## AIM:
To write a Python program using OpenCV to read and display an image, adjust its brightness, modify its contrast, and split the image into Blue, Green, and Red channels.

## Software Required
- Anaconda – Python
- Jupyter Notebook
- OpenCV

## Algorithm

### Step 1: Read and Display an Image
Load the image `sai1.jpeg` from the local directory using OpenCV and display it.

### Step 2: Adjust Brightness
Create a matrix of ones with the `float64` data type to adjust the brightness of the original image.

### Step 3: Generate Brighter and Darker Images
Add and subtract a constant matrix from the original image to create brighter and darker versions. Display all three images.

### Step 4: Modify Image Contrast
Create two contrast-adjusted images using scaling factors of `1.1` and `1.2`, without applying an overflow correction. Display the original and modified images.

### Step 5: Split Image Channels
Split the original image into Blue, Green, and Red (BGR) components and display each channel separately.

## Program Developed By
- **Name:** : SAI PRAVEEN C
- **Registered Number:** 212225230239

## EXP-No-01 :  IMAGE HANDLING AND PIXEL TRANSFORMATION USING OPENCV

##  Read the image ('sai1.jpeg') using OpenCV imread() as a grayscale image:
> ```
> import cv2
> import matplotlib.pyplot as plt
> ```

## Read the saved image above as a color image using cv2.cvtColor():
>```
>img = cv2.imread('sai1.jpeg', cv2.IMREAD_COLOR)
>```

## Original Image:
>```
>img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
>plt.imshow(img_rgb, cmap='viridis') 
>plt.title("Original Image")
>plt.axis('off')  
>plt.show()
>```

## Convert Original Image with line from top left to right bottom
>```
>image = cv2.imread('sai1.jpeg')
>img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
>height, width, channels = img_rgb.shape
>line_img = cv2.line(img_rgb.copy(), (0, 0), (width - 1, height - 1), (255, 0, 0), 2)
>plt.figure(figsize=(8, 6))
>plt.imshow(line_img, cmap='viridis')
>plt.title("Image with Line")
>plt.axis('off')
>plt.show()
>```

## Convert Original Image with Blue Circle:
>```
>image = cv2.imread('sai1.jpeg') 
>img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
>img_rgb.shape
>circle_img = cv2.circle(img_rgb,(600,800),400,(0,0,255),10)
>plt.imshow(circle_img, cmap='viridis')  
>plt.title("Image with Circle")
>plt.axis('off')  
>plt.show()
>```

## Convert Original Image with RED Rectangle border:
```
>image = cv2.imread('sai1.jpeg')
>img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
>img.shape
>rectangle_img = cv2.rectangle(img_rgb, (0, 0), (1200, 1600), (255, 0, 0), 20)
>plt.imshow(rectangle_img, cmap='viridis')  
>plt.title("Image with Rectangle")
>plt.axis('off')  
>plt.show()
```
## Convert Original Image with Text:
>```
>import cv2
>import matplotlib.pyplot as plt
>image = cv2.imread('sai1.jpeg')
>img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
>text_img = cv2.putText(img_rgb, "SAI PRAVEEN C", (50, 120), cv2.FONT_HERSHEY_SIMPLEX, 3, (255, 255, 255), 6)
>plt.imshow(text_img, cmap='viridis')  
>plt.title("Image with Text")
>plt.axis('off')  
>plt.show()
>```

## Convert Original Image into RGB:
>```
>image = cv2.imread('sai1.jpeg')
>image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
>plt.imshow(image_rgb)
>plt.title("Original RGB Image")
>plt.axis("off")
>```
## Convert Original Image into HSV:
>```
>image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
>plt.imshow(image_hsv)
>plt.title("HSV Image")
>plt.axis("off")
>```

## Convert Original Image into GrayScale:
>```
>image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
>plt.imshow(image_gray, cmap='gray')
>plt.title("Grayscale Image")
>plt.axis("off")
>```

## Convert Original Image into YCrCb:
>```
>image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
>plt.imshow(image_ycrcb)
>plt.title("YCrCb Image")
>plt.axis("off")
>```

## Convert HSV Image into RGB:
>```
>image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
>plt.imshow(image_hsv_to_rgb)
>plt.title("HSV to RGB Image")
>plt.axis("off")
>```

## Convert Image with Center White Block:
>```
>image[500:1100, 300:900] = [255, 255, 255]
>image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
>plt.imshow(image_rgb)
>plt.title("Image with 300x300 White Block")
>plt.axis("off")
>plt.show()
>```

## Re-Sized Image (Half):
>```
>image = cv2.imread('sai1.jpeg')
>image.shape
>resized_image = cv2.resize(image, (1200 // 2, 1600 // 2))
>resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
>resized_image_rgb.shape
>plt.imshow(resized_image_rgb)
>plt.title("Resized Image (Half Size)")
>plt.axis("off")
>plt.show()
>```

## Cropped Region of Interest (ROI):
>```
>image = cv2.imread('sai1.jpeg')
>image.shape
>roi = image[200:800, 200:800]
>roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
>plt.imshow(roi_rgb)
>plt.title("Cropped Region of Interest (ROI)")
>plt.axis("off")
>plt.show()
>```

## Image Flipped Horizontally: 
>```
>image = cv2.imread('sai1.jpeg')
>flipped_horizontally = cv2.flip(image, 1)
>flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
>plt.imshow(flipped_horizontally_rgb)
>plt.title("Flipped Horizontally")
>plt.axis("off")
>```

## Image Flipped Vertically:
>```
>flipped_vertically = cv2.flip(image, 0)
>flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
>plt.imshow(flipped_vertically_rgb)
>plt.title("Flipped Vertically")
>plt.axis("off")
>```

