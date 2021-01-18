# NPRG067-Course-project-2

Following repository suppose to store the second of two mandatory semestral projects from subject NPRG067 - Python for practice, necessary to obtain the course credit.

## Siamese networkds + One-shot classification - Assignment description

Purpose of this assignment is to design, train, implement and test siamese network for needs of one-shot classification (A classification based on only one known example for certain classes). One-shot classification is necessary especially in situation when number of classes can change dynamicaly and therefore is not possible to re-train the model for each of the particular classes (for instance a visual identification of all employees of some large company). For those situation is possible to use an alternative of Siamese networks (i.e, [Siamese Networks - WIKI](https://en.wikipedia.org/wiki/Siamese_neural_network)), which specialize on binary clasification of pairs of objects.

<br/>

Your solution will be built on top of Fashion-MNIST dataset ([fashion-mnist dataset](https://github.com/zalandoresearch/fashion-mnist)) or the MNIST dataset.

<br/>
### Assignment requirements
- Create model of Siamese network (expectation on use ***tf.keras***)
- Train the model on Fashion-MNIST dataset (train set needs to be adjusted for the needs of **binary classification**)
- Extend the Fashion-MNIST dataset by a new classes (more details below)
- Test the model on the both, the original dataset and the representatives of the new categories
- Report an achieved results and explore the influence of hyper-parameters of the model on the results

<br/>

Minimal precision of the model on the validation dataset is expected to be *approximatelly 90%*. Scale of extensions of **Fashion-MNIST** dataset is let upon your decission and design, however it is required to introduce at least 10 new classes, which will be disjoint with the original dataset. Those classes suppose to extend the domain of the mode (watches, hats, etc.), or are related to another domain (for instance furniture). From each class choose at least 10 representative and convert them **Fashion-MNIST** format ***(greyscale, 28x28)***. For this you may want to use a subset of **ImageNet** dataset. From each class then chose one representative (***known class member***) which will be used for testing against the rest of the data (it means that you do not re-train the network for new classes, but you investigate distances between *known representatives* and new data). 
