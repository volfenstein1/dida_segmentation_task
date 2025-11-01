# dida_segmentation_task

From the description of the task:

> There are 30 satellite pictures of houses and 25 corresponding labels that
> indicate the roofs. Take those 25 data points and train a neural network on
> them - you are completely free about the architecture and are of course
> allowed to use any predefined version of networks, however, you should be
> able to explain what you are doing - in terms of code as well as in terms
> of why certain steps are good choices. The preferred language is Python,
> but you can also use other languages. Please evaluate your network on the 5
> remaining test images by making predictions of the roofs - send us the
> predictions and ideally some comments on what you have been doing.
> Everything else we will discuss from there.

This repository contains my model training scripts for this task.

1. Initial baseline - I fix initial choices for the segmentation model, write a training loop, and define evaluation across various metrics. I also show how to make predictions on the unlabeled images.
2. Iteration and experimentation - I perform experiments to iteratively improve upon the modeling choices. In order, I experiment with the model encoder and pretrained weights, the model architecture, the optimizers, and the loss function. I also defined a rudimentary dashboard (plots.html) to interactively plot these results and summarize my experimental findings.
3. Final training and augmentation test - Having fixed informed modelling choices, this notebook contains the final training of the model. I also perform one final experiment of a control model, and a model trained on augmented data from the dataset, attempting to mitigate our original datasets small size. The control performed better, and so I made the final predictions using this control model.

For background information on this task, I learned a lot from Damek Davis's notes [A Playbook for Tuning Deep Learning Models](https://damek.github.io/STAT-4830/section/11/notes.html) and the [write-up](https://medium.com/kaggle-blog/carvana-image-masking-challenge-1st-place-winners-interview-78fcc5c887a8) of the first place winners of the Kaggle competition
[Carvana Image Masking Challenge](https://www.kaggle.com/competitions/carvana-image-masking-challenge/overview).

If you prefer, you can also view these notebooks on my website [here].
