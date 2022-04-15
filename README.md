# SAAS-Google-Cloud-Vision-API

URL: [https://saas-app-007.uc.r.appspot.com)


## App Running


![Screen Shot Example](images/2.png)

![Screen Shot Example](images/1.png)



## Explanation

### Creating Cloud Set-Up

Create a new project in your Google cloud console.

Add your Project Name

![Screen Shot Example](images/3.png)
Click Create

![Screen Shot Example](images/4.png)

Go to Your Project,then
From Navigation menu Go to

	App Engine => Dashboard

![Screen Shot Example](images/5.png)

Click Create Appliaction	

![Screen Shot Example](images/6.png)

In language select Java

![Screen Shot Example](images/7.png)

Click Next. Then Go To API Services 

![Screen Shot Example](images/8.png)

Search for Cloud Vision

![Screen Shot Example](images/9.png)



![Screen Shot Example](images/10.png)

Search Cloud Vision API

![Screen Shot Example](images/11.png)

Enable API

![Screen Shot Example](images/12.png)

Go to IAM & Admin 

![Screen Shot Example](images/13.png)

Go to Service Account

![Screen Shot Example](images/14.png)

Create service

![Screen Shot Example](images/15.png)
Go to APIs & Services => Credentials => Create credentials
![Screen Shot Example](images/16.png)
![Screen Shot Example](images/17.png)



### Ecllipse Setup & Project Explannation

Go to App Engine in the ecllipse.
Click on Create New Project

Go to Google App Engine Standard Java Project
Add your Project name.
![Screen Shot Example](images/e1.png)


Check Create as Maven Project.


![Screen Shot Example](images/e2.png)

![Screen Shot Example](images/e3.png)

Add neccessary dependencies in pom.xml file. In this google-cloud-vision - artifact is necessary for detecting labels. 

After that create application jsp pages and their corresponding servlets.
index.jsp: This page allows to upload image to the application.
The Upload.java servlet gets the requests. 



**index.jsp** - Allows us to upload an image.

**Upload.java** - It is a servlet that gets the request. After receiving the request, the image is converted to blobbytes. BLOB allows us to manage the creation and serving of large, immutable blobs to users. After that it is processed in the method getImageLabels() in order to to fetch the image labels  by using the Google CV api. The fetched label results are then redirected to the view using labels.jsp

**BlobstoreService** - 

com.google.appengine.api.blobstore
BLOB - Binary Large OBject.BLOB is a collection of binary data that is stored as a single entity.

[https://cloud.google.com/appengine/docs/standard/java/javadoc/com/google/appengine/api/blobstore/BlobstoreService](https://cloud.google.com/appengine/docs/standard/java/javadoc/com/google/appengine/api/blobstore/BlobstoreService)
 

**Send feedback AnnotateImageRequest** - This API requests for performing Google Cloud Vision API tasks over a user-provided image, with user-requested features, and with context information.

[https://cloud.google.com/vision/docs/reference/rest/v1/AnnotateImageRequest](https://cloud.google.com/vision/docs/reference/rest/v1/AnnotateImageRequest)




After creating app deploy your project to google cloud in the cloud project created.
![Screen Shot Example](images/e4.png)


### State of system :- This application runs properly and able to detect images


 