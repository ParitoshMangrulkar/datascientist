# Pillow - Image Processing

pip install Pillow
from PIL import Image
im = Image.open("test.png")

im.getbands()
('R', 'G', 'B')

im.mode
'RGB'

im.size
(400, 600)

### Image to STRING:

import base64

with open("test.jpg", "rb") as image:
    image_string = base64.b64encode(image.read())
    
### String to Image
import io

image = io.BytesIO(base64.b64decode(image_string))
Image.open(image)

### Create Thumbnail

size = 128, 128
im.thumbnail(size)
im.save('test.png')


### Crop

im = Image.open('test.jpg')
box = (100, 150, 300, 300)
cropped_image = im.crop(box)
cropped_image



### Rotate

rotated = im.rotate(180)
rotated



### Merge

logo = Image.open('logo.png')

position = (38, 469)
im.paste(logo, position)
im.save('merged.jpg')


image_copy = image.copy()


### background
im = Image.open("test.jpg")
image_copy = im.copy()
position = ((image_copy.width - logo.width), (image_copy.height - logo.height))
image_copy.paste(logo, position,logo)
image_copy

















