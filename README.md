# CardsDetection
![card](https://github.com/Vviet21/CardsDetection/assets/96041524/235eb135-9f93-4d72-9158-0f5f817582f0)
## Train
First you need to initialize submodule by running the 2 following commands:

- git submodule init

- git submodule update

As the next step, you need to download the dataset at [dataset](https://universe.roboflow.com/augmented-startups/playing-cards-ow27d/dataset/1). Then you need to extract the downloaded one and rename it to PlayingCards and move it to datasets folder

Then run the following command to copy necessary files to yolov5 folder:

- cp datasets/playing_cards.yaml yolov5/data/playing_cards.yaml
- cp modified_detect.py yolov5/modified_detect.py
- cp playing_cards.pt yolov5/playing_cards.pt
- cd yolov5
  
Finally you could start the training by running:

- train.py --img 800 --batch 8 --epochs 100 --data playing_cards.yaml --weights card.pt --rect
