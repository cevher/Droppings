This repo contains the original dataset of cattle droppings collected from 3 different private farms in Nigde. The purpose of the study is to count the undigested grains found in the cattle dropping. The high number indicates inefficient use of high priced feeding stuff or a digestion problem of cattle. 

The source code and data are readily available in the repo. 

Two different Neural Network Architectures are used. All codes are written in Pytorch. And some repos and studies of other researchers are benefitted during coding process. Those can be seen in the following links.
1- https://github.com/WeidiXie/cell_counting_v2
2- https://www.robots.ox.ac.uk/~vgg/research/counting/index_org.html
3- https://neurosys.com/blog/objects-counting-by-estimating-a-density-map
4- https://personal.ie.cuhk.edu.hk/~ccloy/downloads_mall_dataset.html
5- http://www.svcl.ucsd.edu/projects/peoplecnt/

Anyone who wants to use this repo should follow these steps. 
1- dowload repo content
2- pip install requirement.txt
3- Use utils.ipynb to preprocess and split train test data.
4- python  train.py --dataset_name [preprocessed train data folder]  --network_architecture [UNet|FCRN_A] --learning_rate [float number] --epochs [integer value]  --batch_size [integer value]  --plot [to visualize process]   --help [to see usage directive]

Once the training done.
5- python infer.py -n [UNet|FCRN_A] -c [produced pth file] -i [route to the image to be predicted] --visualize  [to display resulting heat map image]
