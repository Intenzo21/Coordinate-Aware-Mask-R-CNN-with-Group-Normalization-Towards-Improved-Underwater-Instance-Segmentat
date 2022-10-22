# Coordinate-Aware Mask R-CNN with Group Normalization: Towards Improved Underwater Instance Segmentation

We propose a novel hybrid Instance Segmentation (IS) method, called Coordinate-Aware Mask R-CNN (CAM-RCNN), which is motivated by the Mask R-CNN (MRCNN) and Segmenting Objects by LOcation v2 (SOLOv2) algorithms. CAM-RCNN’s structure is mainly constructed on MRCNN with modifications replicated from SOLOv2’s architecture. To this end, we extend MRCNN by introducing a CoordConv layer, multiple Group Normalization (GN) data normalisation layers, and the unique compound DiceBCE Loss (DBL) function to its mask prediction branch. We also present a box-based version of SOLOv2’s mask-based Matrix Non-Maximum Suppression (MNMS), termed Matrix Bounding Box Non-Maximum Suppression (MBBNMS), which replaces the original Batched NMS (BNMS) of MRCNN applied to its predicted region proposals. For training and evaluation, we adopt several real-world unique aquatic datasets provided by the University of Aberdeen. Along with the aforementioned models, we consider two other State-Of-The-Art (SOTA) techniques, namely CenterMask and Conditional Convolutions for Instance Segmentation (CondInst), to better validate our findings. Our results indicate that CAM-RCNN achieves an outstanding test set generalisation performance compared to the other SOTA architectures on almost all evaluation metrics considered. Particularly, the finalised CAM-RCNN model demonstrates over 2.5× (177.3%) and 31.9% increase in instance mask Average Precision (AP) regarding the worst and best performing baseline models, respectively. Our proposed CAM-RCNN is promising to be a generic approach for IS-related applications.

## Installation

1. Install the latest [conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html) (Anaconda);
2. Download the source code and extract to the desired location;
3. Enter an Anaconda Prompt terminal window in administrator mode;
4. Navigate to the source code directory;
5. Create the **aquatic** (default) conda environment by running:
    
    ```
    conda env create -f environment.yml
    ```
    
  - Alternatively, to change the default conda environment name use:
  
    ```
    conda env create -n <env_name> -f environment.yml
    ```
    where **<env_name>** should be replaced with the new custom name of the environment.

6. Activate the project conda environment via:
    
    ```
    conda activate <env_name>
    ```
    where **<env_name>** is as above.

7. Run a script file (dataset and COCO pretrained model weights are needed).
* [demo.py](https://github.com/Intenzo21/Coordinate-Aware-Mask-R-CNN-with-Group-Normalization-Towards-Improved-Underwater-Instance-Segm/blob/main/demo.py) - Script for creating demo inference videos.
* [inspect_results.py](https://github.com/Intenzo21/Coordinate-Aware-Mask-R-CNN-with-Group-Normalization-Towards-Improved-Underwater-Instance-Segm/blob/main/inspect_results.py) - Script used for inspecting loss results along with validation and
test set output metrics of a model.
* [plot_dist.py](https://github.com/Intenzo21/Coordinate-Aware-Mask-R-CNN-with-Group-Normalization-Towards-Improved-Underwater-Instance-Segm/blob/main/plot_dist.py) - Script plotting the data distribution across the training, validation and test sets.
* [run_amsrcr.py](https://github.com/Intenzo21/Coordinate-Aware-Mask-R-CNN-with-Group-Normalization-Towards-Improved-Underwater-Instance-Segm/blob/main/run_amsrcr.py) - Script that runs the AMSRCR image enhancement technique on a given image dataset.
* [train_eval_model.py](https://github.com/Intenzo21/Coordinate-Aware-Mask-R-CNN-with-Group-Normalization-Towards-Improved-Underwater-Instance-Segm/blob/main/train_eval_model.py) - Script used for training an instance segmentation model.
* [visualize_json_results.py](https://github.com/Intenzo21/Coordinate-Aware-Mask-R-CNN-with-Group-Normalization-Towards-Improved-Underwater-Instance-Segm/blob/main/visualize_json_results.py) - Script used for visualising model JSON IS results (i.e. coco_instances_results.json).

## Manuals

* [Maintenance manual](https://github.com/Intenzo21/Coordinate-Aware-Mask-R-CNN-with-Group-Normalization-Towards-Improved-Underwater-Instance-Segm/blob/main/manuals/maintenance_manual.pdf)
* [User manual](https://github.com/Intenzo21/Coordinate-Aware-Mask-R-CNN-with-Group-Normalization-Towards-Improved-Underwater-Instance-Segm/blob/main/manuals/user_manual.pdf)
