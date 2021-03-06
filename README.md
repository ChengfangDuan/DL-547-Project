## Deep Learning Project Code Instruction
---
#### Before running
- Data preparation (download and unzip)
    - [2014 Train images [83K/13GB]](http://images.cocodataset.org/zips/train2014.zip)
    - [2014 Val images [41K/6GB]](http://images.cocodataset.org/zips/val2014.zip)
    - [2014 Train/Val annotations [241MB]](http://images.cocodataset.org/annotations/annotations_trainval2014.zip)
- Folder Structure
    - Git Repo
        - caption.py
        - create_input_files.py
        - datasets.py
        - eval.py
        - models.py
        - train.py
        - utils.py
        - data [folder]
            - train2014 [folder]
                - *.jpg
            - val2014 [folder]
                - *.jpg
            - dataset_flickr30k.json
            - dataset_flickr8k.json
            - dataset_coco.json
        - output [manually add this folder]
---
#### Start running
- step1: generate initial files
    - setting: vim create_input_files.py
        - karpathy_json_path='./data/dataset_coco.json'
        - image_folder='./data'
        - output_folder='./output'
    - running: python create_input_files.py
- step2: training model
    - setting: vim train.py
        - data_folder = './output'
    - running: python train.py
