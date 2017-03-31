# Fully Convolutional Networks for Image Segmentation

The document can be viewed as a rendered markdown [here](https://github.com/warmspringwinds/scipy_talk_austin/blob/master/main.md).

### Abstract
Recently, a considerable advancemet in the area of Image Segmentation was achieved after state-of-the-art methods based on Fully Convolutional Networks (FCNs) were developed. The objective of Image Segmentation problem is to label every pixel in the image with the class of its enclosing object or region. This problem is extremely challenging because the method should have strong classification and localization properties at the same time. While being very complicated, image segmentation is an important problem as it has many applications in medicine, autonomous driving and other fields. In our talk, we go through theory of the recent state-of-the-art methods for image segmentation based on FCNs and present our library which aims to provide a simplified way for users to apply these methods for their own problems.

### Detailed description

#### Background
Methods based on Convolutional Neural Networks (CNNs) have pushed the performance on a broad array of problems, including image classification [(1)][cnn_krizh]  and object detection [(2)][detect_girsh].  ImageNet Large Scale Visual Recognition Competition (ILSVRC) is a main image classification competition. The training data of ILSVRC contains 1000 categories and approximately 1.2 million images and all successful approaches that perform well on this dataset are based on CNNs. Moreover, CNNs that were trained on this dataset act as a good initialization for other tasks as object detection, image segmentation and others [(2)][detect_girsh] [(3)][long_fcn]. 

However, partial built-in invariance of CNNs to translations, rotations and other transformations made it hard to use pretrained CNNs for the task of image segmentation. While being beneficial for the task of image classification, invariance properties are not beneficial for the task of image segmentation where strong localization propoerties are required [(3)][long_fcn].

Recent work introduced Fully Convolutional Networks [(3)][long_fcn], an adaptation of image classification CNNs that enables to successfully use them for the task of image segmentation while reducing the negative effect of invariance properties. In our talk, we briefly describe basic building blocks of CNNs (convolutional layers, pooling layer, fully connected layers etc.), explain why they show superior performance according to recent papers, explain how these CNNs can be converted into FCNs in order to perform image segmentation. After that we conclude with demonstration of how our library can be used to train FCNs for image segmentation on a particular dataset.

### Talk overview.

We plan to structure our talk in the following way:
 - Basic building blocks of Convolutional Neural Networks (CNNs) based on "A guide to convolution arithmetic for deep learning" resource [(4)][conv_guide].
 - Live demonstration on how these CNNs can be applied for image classification based on our blog post [(5)][cnn_class].
 - Live demonstration and explanation on how CNNs can be converted into FCNs based on our blog post [(5)][cnn_class]. 
 - Live demonstration and explanation on how interpolation can be reformulated in terms of convolution and being integrated into the network architecture based on our blog post [(6)][upsampling].
 - Live demonstration and explanation on how FCNs can be trained on the PASCAL VOC general image segmentation dataset based on our blog post [(7)][fcn_training].
 - Demonstration of how our library [(8)][our_library] (implemented using Tensorflow library) was used to train these models for the task of segmentation of medical images based on our recent paper [(9)][our_paper].


### Conclusion and discussion

In our talk, we introduced audience to the recent advancement in the field of image segmentation research, breifly covered the theory behind it and showed how some of the recent state-of-the-art image segmentation methods can be applied to a particular task using our library.

### Biography and additional information

Daniil Pakhomov is a PhD student at Johns Hopkins University. His main research area is general image segmentation and segmentation of medical images.

Contents of our blog posts were well-accepted by machine learning community. Some of them got a promotional tweets from the official Kaggle account and others [(10)][twitter]. The author previously gave a talk on EuroScipy 2016 conference [(11)][euro_scipy].

   [tf_img_segm]: <https://github.com/warmspringwinds/tf-image-segmentation>
   [long_fcn]: 
<https://people.eecs.berkeley.edu/~jonlong/long_shelhamer_fcn.pdf>
   [deeplab_fcn]: 
<https://arxiv.org/abs/1412.7062>
   [cnn_krizh]: 
<http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf>
   [detect_girsh]: <http://www.cv-foundation.org/openaccess/content_cvpr_2014/papers/Girshick_Rich_Feature_Hierarchies_2014_CVPR_paper.pdf>
   [obj_detect_module]: 
https://github.com/scikit-image/scikit-image/pull/1570
   [conv_guide]: 
<https://arxiv.org/pdf/1603.07285.pdf>
   [cnn_class]: 
<http://warmspringwinds.github.io/tensorflow/tf-slim/2016/10/30/image-classification-and-segmentation-using-tensorflow-and-tf-slim/>
   [upsampling]: 
<http://warmspringwinds.github.io/tensorflow/tf-slim/2016/11/22/upsampling-and-image-segmentation-with-tensorflow-and-tf-slim/>
   [fcn_training]: <http://warmspringwinds.github.io/tensorflow/tf-slim/2017/01/23/fully-convolutional-networks-(fcns)-for-image-segmentation/>
   [our_paper]: <https://arxiv.org/abs/1703.08580>
   [our_library]: <https://github.com/warmspringwinds/tf-image-segmentation>
   [twitter]: <https://twitter.com/warmspringwinds>
   [euro_scipy]: <https://www.euroscipy.org/2016/schedule/sessions/13/>