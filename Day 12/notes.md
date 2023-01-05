# NOTES
===========



### Links:
-----------
1. https://www.deeplearning.ai/ai-notes/initialization/index.html
2. https://www.analyticsvidhya.com/blog/2021/05/how-to-initialize-weights-in-neural-networks/
3. https://mlc.ai/
4. https://scholar.google.com/citations?hl=en&user=7nlvOMQAAAAJ&view_op=list_works&sortby=pubdate
5. optimization https://www.deeplearning.ai/ai-notes/optimization/index.html
6. batch normalization https://machinelearningmastery.com/using-normalization-layers-to-improve-deep-learning-models/
7. https://datahack.analyticsvidhya.com/contest/job-a-thon-january-2023/?utm_source=blog_india&utm_medium=desktop_popup&utm_campaign=04-Jan-2023||&utm_content=announcement
8. dropout regularization video https://youtu.be/lcI8ukTUEbo
9. mnist https://en.wikipedia.org/wiki/MNIST_database
10. 3BLUE1BROWN video about mnist https://youtu.be/aircAruvnKk
11. what is convolution? https://mathworld.wolfram.com/Convolution.html
12. https://in.mathworks.com/videos/introduction-to-deep-learning-what-are-convolutional-neural-networks--1489512765771.html
13. https://www.v7labs.com/blog/data-augmentation-guide
14. 
15. 
16. 


### Notes on MNIST with CNN using :
* last value at last is the channel defined by tensorflow
* this channel is used in input_shape
* 16 filters in convolution
* we perform MaxPooling with 2x2
* 10 percent drop out
* 512 (10%) 200 (20%) 10 at last


### CFIR-10 :
* colored images
* 3 channels R G B
* activation matrix will be 2 D


### Image Classification using new method :
* create folders/directories based on category
* train folder must have every category with its own folder
* test folder will have the same
* keras has a preprocessing class ImageDataGenerator to convert images into digial data point 
* batch wise operations are done
* class_mode 
	- binary
	- categorical
* adding batch normalization can improve validation accuracy 
* Model is overfit
	- Restoring model weights from the end of the best epoch: 4. 18/18 - 10s - loss: 0.0626 - accuracy: 0.9820 - val_loss: 1.0336 - val_accuracy: 0.5571 - 10s/epoch - 544ms/step Epoch 9: early stopping
	
### Celebrity Image
* images are not separted into test and train so we use ImageDataGenerator to make _subset_
* we used these subsets and greated two generators
	- train_generator
	- test_generator
* still data is not that enough sometimes, the model overfits 
* we can opt to add more params in ImageDataGenerator to _augment_ the data
* we have normalization, shifting, rotating, shearing options [from here]( https://www.tensorflow.org/versions/r2.9/api_docs/python/tf/keras/preprocessing/image/ImageDataGenerator#:~:text=train_datagen%20%3D%20ImageDataGenerator())
* 