# Bill_Maker_For_FMCG_Stores
An ML application that is hosted on cloud &amp; edge computing devices able to generate the bill receipt using Object detection


  Please reach me if anyone wants to collaborate for the Future Scope!

  #Contact: +91 9488641192 (WhatsApp)

  EDGE COMPUTING – SOLUTION

INFRAMIND 2019

Team Name: _ATOM_

from Bannari Amman Institute of Technology

Team Members

Balamurugan T (Bala) , Engineer, Call : +91 9488641192 ( Whatsapp) Fractal
tbala2805@gmail.com
Praveen V  Engineer, TCS, Call: 8883168568
praveen241298@gmail.com

   
Introduction
Now a days in retail shops workers spend more time in checkout systems.
Billing counters are not much user friendly for workers because of this customer
spend more time in billing counters to bill their products. And also delayed
checkout system will affect the sales of the retail stores.

Existing system
In retail shops presently using barcode scanners to quickly finish the
checkouts. But it is not the fastest way of doing checkouts. Some of the
disadvantages are
 Cannot able to find damaged labels.
 Different products have barcodes in different sides so workers have to search
for barcodes in products, so it takes time to scan different products.
 Not able to scan many products at a same time, products must be scanned
one by one.

Proposed System
The proposed system uses edge computing along with machine learning
technology to automate the checkout system. This system identifies the product by
capturing image of the product and process the image using neural networks.
The machine learning model detect the product with respect to brand and size of
the product.




Details of technology Used
The technologies used to make the system are listed below
 Image processing
 Deep learning
 Edge computing
 Web technology


Image processing
Image processing technology is used to capture and process the image before
giving input to the neural network. And also, image processing technique is used to
find the size of the product by comparing with the reference object on the same
plane.
Deep learning
Deep learning technology is the heart of this system. A deep learning model
is trained to detect the various products on the store. For deep learning we are
using Darknet yolo model, this yolo model is best suitable for real time object
detection.

Edge computing
Edge computing technology is used to process the captured image in neural
network closer to the retail store to reduce the latency which occurs during the
cloud computing. The server which process the image and the web server and
neural network is located inside or closer to retail store.
Web technology
Web application is created to capture the image of the product and to show
the billing details of each product. Web application capture the image send image
to the sever and show the results returned from the server.


Required Software /Hardware
Software and hardware required for this system are listed below
 Laptop
 Web camera
 Xampp
 Darkflow (github repository)
 Python 3.7
o Tensorflow
o Opencv
o Numpy
o Mysql connector

Xampp
Xampp is a software installed in laptop to host web server in a laptop.
Xampp runs apache web server in port 8080 and 443. And also, xampp runs the
mysql database in the local machine to store the data of the image captured and
product details identified from image by neural network.
Darkflow
Darkflow is the github repository which provides the machine learning
model for object detection. We trained this available model to detect the various
products available in the retail store. Darkflow uses yolo (you look only once)
model for object detection. Github link: https://github.com/thtrieu/darkflow

Python

6

Python language is used to load the machine learning model along with the
weights trained and detect the product. The identified product label is stored in the
database using mysql connector library. The size of the product is identified by
processing the image using the opencv and numpy library.
Architecture of Neural Network
• Convolution Neural Network:
⮚ Convolution layers
⮚ Pooling layers
• Fully connected Neural
Network:
⮚ Flatten layers
⮚ Hidden layers
⮚ Output layer
⮚ Activation function
⮚ Relu activation function - Hidden layers
⮚ Softmax activation function -Output layers

Solution Brief Description:
Client Side:
live video feed from the camera.
 Worker take a snapshot of the product and the add to the cart by using take
snapshot and add button in web application after product is placed in front
of the camera.
 After all products are added to the cart user will submit the images using
submit button.
 On successful submission the images are submitted in base64 string format.
 If the detection process is completed the present webpage redirects to billing
page which shows the bill for the submitted products.
Server Side
 When submit button is pressed php script receives the image in base64 string
format and then image is decoded and stored in local storage and location,
Id, image status and image name is updated into the database.
 Parallelly python program running on the machine which detect the change
in the database.
 Python script get the image details from the database and run the neural
network to detect the product. After detection, the label and size of the
product is updated to the database.
 Php script get the label detail from the database and compared with the
available products and shows the bill to the user.
 The size of the object is detected by comparing the size of the reference
object with the product.
 The reference object and product must be in same plane to find the exact
size of an object.
Scope of Automation

10

 This system able to find the products by manually taking pictures of
products this will be automated in future design.
 System will be improved to detect many products from single image taken
from the camera this will reduce the time further.
 By applying above improvements, we can automate the full checkout
process without any human actions.

Conclusion
The proposed system will be better when compared to the existing system
and it will reduce the time of customers in queue. Because of the deep learning
method used in the system it will have high accuracy than any other systems.
