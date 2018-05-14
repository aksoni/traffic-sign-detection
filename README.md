# Red Traffic Sign Detection using TensorFlow Object Detection API

This system detects red traffic signs in the [GTSDB database](http://benchmark.ini.rub.de/?section=gtsdb&subsection=dataset) using TensorFlow's Object Detection API.

This system was developed with help from Vatsal Sodha's [TensorFlow Object Detection API tutorial — Training and Evaluating Custom Object Detector](https://becominghuman.ai/tensorflow-object-detection-api-tutorial-training-and-evaluating-custom-object-detector-ed2594afcf73).

#### To train the system from scratch:

Delete the model.ckpt files found in the training/ directory.

Then run `python train.py --logtostderr \ 
       --train_dir=training/ \       
 --pipeline_config_path=training/ssd_mobilenet_v1_coco.config`
 
 You may need to update PYTHONPATH for this to run.
 
 
#### To evaluate the model:
 
 Run `python eval.py \
    --logtostderr \
    --pipeline_config_path=training/ssd_mobilenet_v1_coco.config \
    --checkpoint_dir=training/ \
    --eval_dir=eval/`
    
Evaluation can be run simultaneously with training.


#### To visualize the training results:

`tensorboard --logdir=training/`

#### To visualize the eval results:

`tensorboard --logdir=eval/`

