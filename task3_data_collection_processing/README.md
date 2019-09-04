## Converting separate band images into stacked RGB images #####

### Purpose

In order to facilitate the interpretation of images from Landsat8 images, a script was created
to process 7 single band images, into a stacked RGB representation of the images.

### Usage Steps

1) Load the .gz of an image from your order list at EarthExplorer (or alternatively, get a gz 
from the "original_images" folder)
2) Put the gz file into a directory. Each gz file needs to be in a different directory!
3) Untar the file (for Linux users, here is an example: 
```
tar zxvf LC081650592017031001T1-SC20190902133955.tar.gz  -C DIRECTORY )
```
4) You can now execute the load_image.py script, with the following parameters:

	home directory: The directory where you have unzipped your original file
	stacked_image_destination: During the execution of the script, a file with this name will be generated
	type of image generated: Currently, this script can generate three types of images.
	
		1 - Natural Color
	
		2 - Color Infrared (vegetation)

		3 - Vegetation Analysis

		4 - NDVI image

	Refer to 
	https://www.esri.com/arcgis-blog/products/product/imagery/band-combinations-for-landsat-8/?rmedium=redirect&rsource=blogs.esri.com/esri/arcgis/2013/07/24/band-combinations-for-landsat-8
	for more information

	Example execution:  
```
python load_image.py "/home/manuel.mourato/shared_directory/
image_one/" "stacked_file_test.tif" 3
```
5) If you go back to the directory where you have the original images, a new generated image should be there as well.
