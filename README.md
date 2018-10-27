# hardware
Classifying Hardware Images Using CNN's¶
There are hundreds of different types of hardware items, and many of them are not commonly known by most people. In some cases, the task of locating a needed piece of hardware can require consulting with several individuals, multiple trips to stores, and a great deal of wasted time. This project attempts to show how image classification could be used to address this issue.

Data
The data comes from processing 5,190 images of hardware items. I planned on scraping the images from hardware store webpages, but this proved problematic. For some items, every image was identical. Others had more than one image, but the number of images was still very limited. Creating a model where most items had from one to five images just is not practical, so I ended up using my camera to take images of each item. I tried to capture images from every angle possible and with different backgrounds. In some images, the item is partially obscured. I used Python Imaging Library (PIL) to process the images by resizing them to a 28 by 28 pixel square. I then converted them to arrays. Two sets of arrays were created: one with a single channel of grayscale values and another with 3 channels (red, green, and blue).

The images all fall into one of five categories, each with approximately 1,000 images.

Hardware Categories:


Cam Connectors

Anchor Screws

Eye Bolt

Extruded U-Bolt

Jack Nut


Data was divided into three groups:

Training set

Validation set (used for validation as model is being trained)

Test set (only used after model is trained)
