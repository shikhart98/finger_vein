# ZNCC Finger vein recognition
Using the SDUMLA data set

Download the data set, and execute the scripts in order:
The dataset folder structure is as follows: (db folder, person number, hand left or right, image name) 
  db
   | 01
   |- left
   |--- finger_01.bmp

#get_all_img_roi.py 
  This will  get the ROI of all images, and create a new folder called gab_roi_db,
  containing the files with the ROI preprocessed with CLAHE and gabor filter
#get_roi_bin.py
  This will get the folder with the gabor filtered images, and binarize them.

#get_similarities.py
  This script will test the files in the chosen folder and save the similarity value between each of the images. 
  It will then create a json file with all the obtained values.
  
#one_vs_n.py
  This script will open the json file generated by get_similarities.py, and identify the classes using the similarity values.
