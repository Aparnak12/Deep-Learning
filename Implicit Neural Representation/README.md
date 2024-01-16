A Multi-Layer-Perceptron (MLP) finds optimal nonlinear basis functions to represent data in an end-to-end manner. Implicit neural representations (AKA coordinate-based representations) are a novel way to parameterize signals of all kinds. Conventional signal representations are usually discrete - for instance, images are discrete grids of pixels, audio signals are discrete samples of amplitudes, and 3D shapes are usually parameterized as grids or voxels, point clouds, or meshes. In contrast, Implicit Neural Representations parameterize a signal as a continuous function that maps the domain of the signal (i.e., a coordinate, such as a pixel coordinate for an image) to whatever is at that coordinate. 

<img width=600 src="https://github.com/Aparnak12/Deep-Learning/assets/51270673/3951dea0-fd05-4cf9-a3dd-2600823fb35e">

We can think of this image as a set of data points 
{ $(x^{(i)} = [x_{1}^{(i)}, x_{2}^{(i)}]^T, y^{(i)})$ } $^{M N}_ {i=1}$, where  $x^{(i)} = [x_{1}^{(i)}, x_{2}^{(i)}]^T$
is the coordinates of the $i$’th pixel and $y^{(i)}$
is the grayscale value for this pixel. This image is 256 × 256 and is provided to you as part of this homework under ‘moon.jpg.’ Our goal in
this section is to learn an MLP that regresses over this image and gives us a continuous function
$f : \mathbb{R}^{2} \rightarrow \mathbb{R}$ such that $f(x^{(i)}) \approx y^{(i)}$ Have in mind the three main code-blocks we talked about in the
class: i.e., define model, define optimizer, regress over data iteratively. I recommend using Google
Colab for this problem, and start from the code already provided to you.
