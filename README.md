# tfrecord
Data Preparation Script for image binary classification using TFRecord


########## Make sure TensorFlow version is up-to-date (1.8) ##########

########## TOTAL 4 .py files needs to be downloaded ##########

# create_validation_and_test_data.py
# load_images.py
# read_tfrecord.py
# run.py

"""
    Instruction:
    
    (IMPORTANT) 
    
    OPTION_1: Download the zip file (skin.zip) from Google Drive and unzip to obtain the 'skin' dataset folder
                "https://drive.google.com/file/d/1xb3xrEg4Zjyg1jGB8b1ElsZ29sLtBzz3/view?usp=sharing"
    
    OPTION_2: Download the raw 'skin' folder from Google Drive
                "https://drive.google.com/drive/folders/1F8EJ5-0NJFR5vDeObVMmJrxAGeQDgjpe?usp=sharing"
                
    This main function in "run.py" is used to: 
    
    (It can be used for all .jpg imagery dataset with two classes, but we will use skin dataset for demo)
    
     1. Create validate and test data and their respective class sub-folder: 
            it will automatically create empty folder to store validate and test datasets
     2. Randomly pick data from train folder and move it to 
            validate and test folder with default ratio (refer to function description)
     3. Read in images from these train, validate, test folders and create their TFRecord respectively in it
     4. Read one image from the train TFRecord file to see if the images and its respective label were stored correctly
     
     Any detailed description of each function called, please refer to its respective module
     
    ################################### Please look at my own path below reference ###################################
    
    :param: dataset_dir:                                  Path of the (skin) dataset folder you had 
                                                            (downloaded from INSTRUCTION)

    :param: train_folder_dir_class_0:                     Path of the train dataset for class 0 folder
                                                            folder will automatically be created when called
                                                            just change the path before '/train/benign'
    
    :param: train_folder_dir_class_1:                     Path of the train dataset for class 1 folder
                                                            folder will automatically be created when called
                                                            just change the path before '/train/malignant'
    
    :param: validation_folder_dir_class_0:                Path of the validate dataset for class 0 folder
                                                            folder will automatically be created when called
                                                            just change the path before '/validate/benign'
                                                            
    :param: validation_folder_dir_class_1:                Path of the validate dataset for class 1 folder 
                                                            folder will automatically be created when called
                                                            just change the path before '/validate/malignant'
    
    :param: test_folder_dir_class_0:                      Path of the test dataset for class 0 folder
                                                            folder will automatically be created when called
                                                            just change the path before '/test/benign'  
                                                                    
    :param: test_folder_dir_class_1:                      Path of the test dataset for class 1 folder
                                                            folder will automatically be created when called
                                                            just change the path before '/test/malignant'
    
    
    :param: tfrecord_dir:                                 TFRecord file directory for train dataset
                                                           this TFRecord file will automatically be created when called, 
                                                           so just change the path before '/training.tfrecords'
    
    :param: folder_name_class_0: Default is 'benign', no need to change this parameter if use skin dataset
    :param: folder_name_class_1: Default is 'malignant', no need to change this parameter if use skin dataset
    """

    # Change all 8 paths in "run.py" under the main() and call the function
    
    Example:

        dataset_dir='/home/user/Desktop/skin',

        train_folder_dir_class_0='/home/user/Desktop/skin/train/benign',
        train_folder_dir_class_1='/home/user/Desktop/skin/train/malignant',

        validation_folder_dir_class_0='/home/user/Desktop/skin/validate/benign',
        validation_folder_dir_class_1='/home/user/Desktop/skin/validate/malignant',

        test_folder_dir_class_0='/home/user/Desktop/skin/test/benign',
        test_folder_dir_class_1='/home/user/Desktop/skin/test/malignant',

        tfrecord_dir='/home/user/Desktop/skin/train/training.tfrecords'
 
