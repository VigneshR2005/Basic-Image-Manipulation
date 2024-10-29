# Basic-Image-Manipulation

# Program :
```
import cv2
from matplotlib import pyplot as plt
image = cv2.imread('apollo.jpg', cv2.IMREAD_GRAYSCALE)
height, width = image.shape
print("Width:", width)
print("Height:", height)
plt.figure(figsize=[10, 10])
plt.imshow(image, cmap='gray')
plt.axis('off') 
plt.show()
cv2.imwrite('apollo.png', image)
image = cv2.imread('apollo.jpg')
text = 'Apollo 11 Saturn V Launch, July 16, 1969'
font_face = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
font_thickness = 2
text_color = (0, 255, 0) 
text_size, _ = cv2.getTextSize(text, font_face, font_scale, font_thickness)
text_x = (image.shape[1] - text_size[0]) // 2
text_y = image.shape[0] - 50  
cv2.putText(image, text, (text_x, text_y), font_face, font_scale, text_color, font_thickness)
rect_color = (255, 0, 255) 
top_left = (500, 100)
bottom_right = (700, 600)  
cv2.rectangle(image, top_left, bottom_right, rect_color, 5)
plt.figure(figsize=[12, 12])
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()
```

## OUTPUT :
![download](https://github.com/user-attachments/assets/52200c01-45e3-4e83-abc9-ac3533f01ed8)


![download](https://github.com/user-attachments/assets/7f5fd910-d39e-44a8-98f7-d2906f34e817)


## Exercise 02 :

# PROGRAM :
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('Emerald_Lakes_New_Zealand.jpg', cv2.IMREAD_COLOR)
print("Original image shape:", img.shape)
gray_img = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
print("Grayscale image shape:", gray_img.shape)
plt.figure(figsize=(10, 10))
plt.subplot(121)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis('off')
plt.subplot(122)
plt.imshow(gray_img, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')
plt.show()
x, y, w, h = 250, 100, 300, 200
cropped_img = img[y:y+h, x:x+w]
resized_img = cv2.resize(cropped_img, None, fx=2, fy=2)
flipped_img = cv2.flip(resized_img, 1)
plt.figure(figsize=(5, 5))
plt.imshow(flipped_img[:, :, ::-1])   
plt.yticks([0, 50, 100, 150, 200, 250, 300, 350])  
plt.xticks([0, 50, 100, 150, 200, 250, 300, 350])  
plt.show()
```

# OUTPUT :
![download](https://github.com/user-attachments/assets/97fa3fd3-44dd-4a0e-b0d2-44d2fc343281)


![download](https://github.com/user-attachments/assets/44cbc479-cd77-4df3-bd8b-4ddea53a6554)


![download](https://github.com/user-attachments/assets/61ff64df-96f7-471a-9675-85bcc2f36ce7)

