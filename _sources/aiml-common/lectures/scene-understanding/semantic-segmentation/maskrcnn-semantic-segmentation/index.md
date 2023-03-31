# Mask R-CNN Semantic Segmentation

The semantic segmentation approach described in this section is [Mask R-CNN based on this paper](https://arxiv.org/abs/1703.06870) paper. 

In the object detection section we saw R-CNN that simply cropped proposals, generated externally to the detector, from the input image and classifies  those proposals. Since the proposals were typically overlapping, CNN computations that extracted features per proposal were wasted and the detector was very slow. Fast R-CNN improved this by passing the whole input image once via a CNN feature extractor and used a feature map internally to this CNN to elect proposals, therefore avoiding the feature extraction per proposal. Faster R-CNN removed the external dependency on proposal generation and introduced a Region Proposal Network (RPN) internally to the detector. For the RPN to generate proposals, prior (or anchor)  boxes were defined uniformly across the input image and the RPN was trained to predict the class of each anchor and by how much the anchor needs to shift to match the ground truth bounding box. 


## Implementation and Notebooks

For Tensorflow: 

The four notebooks in this section use MaskRCNN. For other models see [the TF Model Garden](https://github.com/tensorflow/tpu/tree/master/models/official/detection). 

* [This notebook](https://pantelis.github.io/artificial-intelligence/aiml-common/lectures/scene-understanding/semantic-segmentation/maskrcnn-semantic-segmentation/demo) demos MaskRCNN.

* [This notebook](https://pantelis.github.io/artificial-intelligence/aiml-common/lectures/scene-understanding/semantic-segmentation/maskrcnn-semantic-segmentation/inspect_data) visualizes the different pre-processing steps to prepare the training data.

* [This notebook](https://pantelis.github.io/artificial-intelligence/aiml-common/lectures/scene-understanding/semantic-segmentation/maskrcnn-semantic-segmentation/inspect_model) goes in depth into the steps performed to detect and segment objects. It provides visualizations of every step of the pipeline.

* [This notebook](https://pantelis.github.io/artificial-intelligence/aiml-common/lectures/scene-understanding/semantic-segmentation/maskrcnn-semantic-segmentation/inspect_weights) inspects the weights of a trained model and looks for anomalies and odd patterns.

For Pytorch: 

* [This notebook](https://pantelis.github.io/artificial-intelligence/aiml-common/lectures/scene-understanding/semantic-segmentation/maskrcnn-semantic-segmentation/detectron2_tutorial) shows how an existing pretrained model can be used to do instance segmentation on new classes and how video can be processed via a relevant pipeline. The application of transfer learning in Keras is shown [here](https://keras.io/guides/transfer_learning/).

