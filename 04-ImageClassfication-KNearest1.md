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

1.Remember all training images and their labels;
2.Predict the label of the most similiar training image



