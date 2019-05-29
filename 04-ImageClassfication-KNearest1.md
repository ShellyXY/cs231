Image Classification: 
===
**The problem:**
semantic gap

**Challenges:**
>Viewpoint Variation; lllumination; Deformation; Occlusion; Background clutter;  Intraclass variation;

**An image classifier:** 
  no obvious way to hard-code the algorithm for recognizing a cat, or other classes.

  **Data-driven approach**
  1. Collect a dataset of images and labels
  2. Use ML to train an image classifier
  3. Evaluate the classifier on a withheld set of test images

  ```python
  def train(train_images,train_labels):
  #bulid a model for images -> labels...
  return model

  def predict(model,test_image):
  #predict test_labels using the model...
  return test_labels
  ```

**Fisrt classifier:**
 Nearest Neighbor Classifier

1. Remember all training images and their labels;
2. Predict the label of the most similiar training image

**How do we compare the images?**
$d_{1}\left(I_{1}, I_{2}\right)=\sum_{p}\left|I_{1}^{P}-I_{2}^{P}\right|$(曼哈顿距离算法或者是L1距离算法)

The choice of distance is a *hyperparameter*(这里距离的选择我们称作为超参数)

$d_{2}\left(I_{1}, I_{2}\right)=\sqrt{\sum_{P}\left(I_{1}^{P}-I_{2}^{P}\right)^{2}}$(欧几里得距离)

**how do we set the hyperparameters?**
Answer: Very problem-dependent.Must try them all out and see what works best.

拟合程度的选择会影响到分类器的泛化能力

我们会通过比对不同K值下验证集的平均正确率，来得到究竟取多少个近邻值才能得出最准确的结果

**K-Nearest Neighbor on images never used.**
1. terrible performance at test time.
2. distance metrics on level of whole images can be very unintuitive.

