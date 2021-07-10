# GANCartoonAnimator

I customised a linear regression model to take the input for training as well as the required groundtruth.

The GAN model is a sequential Keras Model which takes any random 2048 valued 1-dim array as input and uses it for generating a Cartoon image. The training set of GAN consists of 10000 images extracted from the cartoon dataset.

Now essentially I can have any set of 2048 values and I can have infinite variations in the output image.

The predictor model trains on a linear regression type algorithm to make sense of the HOG features of the input and predicted cartoon Image.

Just by training the linear regression on 100 iterations with 0.005 as learning rate, I got very fascinating results.

The accuracy and other metrics cannot be determined because it needs a seperate non-tradition defination for these metrics.
Here are few results which I obtained.

![download (4)](https://user-images.githubusercontent.com/57591230/125165920-b44a5580-e1b6-11eb-86d1-43c6186c2e4e.png)
![download (5)](https://user-images.githubusercontent.com/57591230/125165923-b6acaf80-e1b6-11eb-8664-2a24d38943c2.png)

There is some amount of overfitting with few features eg. Long Hairs.

![download (12)](https://user-images.githubusercontent.com/57591230/125165938-c4facb80-e1b6-11eb-8756-8efd525a7999.png)
![download (13)](https://user-images.githubusercontent.com/57591230/125165942-c926e900-e1b6-11eb-9af8-09a97fb6da8b.png)
![download (19)](https://user-images.githubusercontent.com/57591230/125165951-dba12280-e1b6-11eb-81f7-785ae1cb9576.png)
![download (20)](https://user-images.githubusercontent.com/57591230/125165953-de9c1300-e1b6-11eb-917c-1cc404565d4a.png)

There are numerous places where this model can be optimised.
1) Training GAN on 30000 cartoons
2) Changing number of iterations in Linear Regression from 100 to 1000
3) Finding the optimal Learning Rate
4) Input data augmentation to find facial region
5) Traing GAN on a different number of input features.

