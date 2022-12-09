# CS686 Final Project 

#### In this project, we will compare three algorithms: Super-Resolution Convolutional Neural Networks (SRCNN), Fast Super-Resolution Convolutional Neural Networks (FSRCNN) and Super-Resolution Generative Adversarial Networks (SRGAN). SRCNN proposed a three-layer convolutional neural network. It directly learns an end-to-end mapping between low/high-resolution images. FSRCNN designed a compact hourglass CNN structure to achieve faster and better SR. And it introduces a deconvolution layer at the end of the network. SRGAN uses a Generative Adversarial network that employs a deep residual network (ResNet) with skip connections and diverges from MSE as the sole optimization objective. We will train and fine-tune these three CNNs (SRCNN, FSRCNN and SRGAN), compare their performance in solving the super-resolution problems on the same situation and discuss their advantages and disadvantages.


## Three Models
-  [Super-Resolution Convolutional Neural Network (SRCNN)](https://arxiv.org/abs/1501.00092)
-  [Fast Super-Resolution Convolutional Neural Network (FSRCNN)](https://arxiv.org/abs/1608.00367)
-  [Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network (SRGAN)](https://arxiv.org/abs/1609.04802)
