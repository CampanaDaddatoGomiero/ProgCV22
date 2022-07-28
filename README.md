# ProgCV22

"data_augmentation.ipynb": it allows to increase the HandOverFace dataset, performing data augmentation. By exploiting the python library Albumentation, three transformations are applied to images contained in "DATASET_AUGMENTATION" folder. The 320 images, in particular, are flipped both horizontally and vertically and changed in terms of brightness.
The tranformed images, together with the corresponding bounding boxes saved into .txt files, are saved into three folders, namely "horiz_flip", "vertic_flip" and "bright".
    
"Convert_BB.ipynb": it is used to convert the bounding boxes associated to the images of the augmented HandOverFace dataset, downloaded from the folder "DATASET_ AUGM_DIVISO". The conversion is made from YOLO to format [x y width height], where x and y are the coordinates of the top left corner of the bounding box. The images, together with the converted bounding boxes, are saved into the folder "HANDOVERFACE", which is finally zipped into "DAT_HANDOVERFACE_DEF".
 
"Detection_YOLOv4.ipynb": it creates the custom object detection network, based on YOLOv4 model. Once built darknet and uploaded all the necessary files into the "darknet" folder, the pre-trained weights are updated during all the training process. The images used to train the network are taken from EgoHands dataset (inside folder "DATASET" in Google Drive) and the augmented HandOverFace dataset (inside directory DATASET_HANDSONFACE).
