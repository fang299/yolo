## Term Paper Project discription

1) How to run the experiments:

     1. Upload .ipynb file onto google drive
     2. Using google colab to open the .ipynb file
     3. The folder contain two .ipynb file, Yolov1 and Yolov2
     4. Upload the PASCAL VOC dataset to desired folder
     5. Run each cells follow the ordered in the file

2) Describe:

    1. Which code files have been copied from other repositories
       In Yolov1 file, the code cells except the first two and the last two cells are copied from the respositories.
       
       In Yolov2 file, the code cells except the first three cells and last two cells are copied from the repositories.
       
       Repositories: https://github.com/aladdinpersson/Machine-Learning-Collection/tree/master/ML/Pytorch/object_detection/YOLO
       
    2. Which code files have been modified and how they have been modified.
    
       Yolov1 file: I modified the train cell.
       
       Train cell:
       
       a. I change the batch size to smaller, so that it won't throw the cuda memory error.
       
       b. Decrease the number of epochs to decrease the runtime.
       
       c. Change the value of if statement for saving the model.
       
       d. Remove the ploting image step in the main function.
       
       Yolov2 file: I modified the model cell and train cell.
       
       Model Cell:
       
       a. change the CNN layer, according to the paper, I replace the last CNN layer in Yolov1 with three layers that there kernel size are 3*3 and output channel are 1024.
       
       Train Cell:
       
       a. I change the batch size to smaller, so that it won't throw the cuda memory error.
       
       b. Decrease the number of epochs to decrease the runtime.
       
       c. Change the value of if statement for saving the model.
       
       d. Remove the ploting image step in the main function.
       
    3. Which code files are the my original code. 
       
       Yolov1:
       
       Test Cell: I create the test function, Load the checkpoint to plot the images. 
       
       In test_fn function I use the model and loss function to calculate the mean loss.
       
       In main function, use the function from previous cell to plot the images and bounding boxes.
       
       Yolov2:
       
       Test Cell: I create the test function, Load the checkpoint to plot the images. 
       
       In test_fn function I use the model and loss function to calculate the mean loss.
       
       In main function, use the function from previous cell to plot the images and bounding boxes.
       
3) Include a description of the datasets you used and where you obtained them.
    
   I use the POSCAL VOC dataset, this dataset is use for object detection, there is 20 classes in total, and there are images folder and label folder, each image in images folder is correpoinding to the text file in label folder. The text file in the label folder contain 5 values, the value is used to indicate the object bounding box of the image. The first value in an integer that indicate which class is this object belongs to. And second and third value indicate the x-axis and y-axis points. The last two values indicate the width and height of the bounding box. 
   
   Obtained from: https://www.kaggle.com/dataset/734b7bcb7ef13a045cbdd007a3c19874c2586ed0b02b4afc86126e89d00af8d2
   
   And I reduce the dataset in images and labels folder to 2000 examples to do the training and testing.
       
       
       
       
       
