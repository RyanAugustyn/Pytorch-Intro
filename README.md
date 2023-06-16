# Pytorch-Intro

Following along to Daniel Bourke's https://www.youtube.com/watch?v=Z_ikDlimN6A.

Machine learning (ml) is turning data into numbers and finding patterns. Where traditional programming turns inputs/rules into outputs, ML turns inputs/outputs into a set of rules.

ML is useful for complex problems where you can't think of all the rules, i.e. every variable in identifying photos of food.

ML is subset of AI, Deep Learning(DL) is subset of ML. Use ML on structured data (rows/columns-algorithm such as XGBoost useful here), DL better for unstructured data(neural network useful here)

From Google ML Handbook: "If you can build a simple rule-based system that doesn't require machine learning, do that."

DL good for: having long lists of rules, continually changing environments, insights with large amts of data

DL bad for: when you need explainability of models (too complex to understand), when the traditional approach is better, when errors are unacceptable (outputs aren't always predictable), or when you have small amounts of data (in most cases)

Common algorithms for both:
ML: random forest, gradient boosted models, Naive Bayes, nearest neighbour, support vector machine, etc
DL: neural networks I(fully connected nn, convolutional nn, recurrent nn), transformer, etc

Neural network: numerical encoding (turn inputs into numbers) called the input layer, learns representations (paterns, features, weights) called the hidden layer(s), representation outputs or the output layer, all of which can produce human readable outputs.

Each layer is usually a combination of linear and/or non-linear functions

Three types of learning:

- supervised (have data such as photos, and labels that tell you what the photos are)
- unsupervised and self-supersized (just data, no labels)
- transfer (taking patterns from one model and transferring to another)

What is PyTorch? Originally designed by Meta, open source Python deep learning framework which is able to run on GPU/many GPUs, access pre-built learning models(Torch Hub/ torchvision.models), and is whole stack (preprocess data, model data, and deploy model)

paperswithcode.com (tracks machine learning papers, useful resource)

GPU(graphics processing unit),often for video games, Nvida CUDA is an api that allows GPUs to be used for general processing, TPUs (tensor processing unit) are also used

What is a tensor? A representation of numbers, think of a box with vectors inside. There are input and output tensors (can have millions of tensors in a model)

Dan Fleisch video (https://www.youtube.com/watch?v=f5liqUk0ZTw), what are tensors?:

- Vector has magnitutde and direction, such as representing force of gravity (amount of force is magnitude, point being pulled to is direction)
- Vectors can also represent areas (length of vector proportional to the amount of the area, then make the direction of the arrow perpendicular to the surface)
  -Vectors are a subset of tensors, to understand need to know vector components and basis vecotrs
  -Basis vectors (or unit vectors) have a length of one (whatever units are being measured). Direction is in the direction fo the coordinate axis. Ex Unit vector along x axis, denoted x^ (or i-hat) points in the direction of increasing x. The j-hat or y coordinate points in the direction of increasing y, and the z-hat or k-hat points in increasing z direction.
  -Vector components: think of a vector on an x/y plane at some angle to the orign. How far x^ and y^ unit vectors does it take to get to the point of the vector itself.
  As an example, a vector [4, 3, 0] would move 4 units in the x direction, 3 in the y, and 0 in the z. Can abstract out to [Ax, Ay, Az]
  -Need one index for each, because only one directional indicator (one basis vector) per component. This makes vectors "tensors of rank one"-meaning one index(unit vector component)
  -Scalars, or quantities having only magnitude, not direction (think of temperature, mass, or energy) are considered to be tensors of rank 0, having no directional indicators
- Can imagine a rank 2 tensor in 3d, have 9 componenents with 9 sets of two basis vectors. Components now have 2 indicies. Could be used to find forces inside a solid object. So Axx might refer to x directed force on a surface whose area vector is in the x direction.
- A rank 3 tensor would have 27 components, so 27 sets of three basis vectors. Axxx pertains to three x basis vectors.
- WHAT makes this so powerful? All observers, in all reference frames, can agree. Not on the basis vectors, not on the components, but on the combination of components and basis vectors.
