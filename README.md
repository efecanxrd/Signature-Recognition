<h2> Signature Recognition </h2>
<h3> Signature recognition using template matching and correlation </h3>
<img src="https://i.imgur.com/qHAcfhX.gif">
<h3> Setup The Project </h3>
 <h4><img align="center" src="https://raw.githubusercontent.com/efecanxrd/efecanxrd/main/images/xe.gif" width="30"> Download Dataset <h4>
<h5> https://www.kaggle.com/datasets/robinreni/signature-verification-dataset </h5>
<h4><img align="center" src="https://raw.githubusercontent.com/efecanxrd/efecanxrd/main/images/xe.gif" width="30"> Install the libraries with pip </h4>
 <h5>pip install tkinter opencv-python pandas numpy Pillow </h5>
<h2> How this is working? </h2>
  <h4>Our code uses the template matching technique in OpenCV to match the signature in an image with the signatures in your dataset.

Our code first loads the image and converts it to grayscale using the cv2.imread and cv2.cvtColor functions. Next, we set a correlation value for template matching.

As our code searches for the signature, it iterates over the folders in the dataset and loads each signature image. The code implements template matching using the cv2.matchTemplate function and checks if a match is found using the correlation value. <br>
This function shifts the template image over the source image and calculates a similarity measure between the template and each region of the source image. The similarity measure used in this case is cv2.TM_CCOEFF_NORMED.

The result of template matching is a 2D array of similarity values. The code uses the np.where function to find all locations in this sequence where the similarity value is greater than or equal to the correlation value.
</h4>
