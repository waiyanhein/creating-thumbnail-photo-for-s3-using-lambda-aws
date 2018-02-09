## Creating thumbnail of photo in Amazon s3 bucket using AWS Lambda ##

### 1. Create the role with the required Permission ###
![picture alt](https://github.com/waiyanhein/creating-thumbnail-photo-for-s3-using-lambda-aws/blob/master/Screenshot%20(76).png)

### 2. On s3, create two bucket <name> and <name>resized
  ![picture alt](https://github.com/waiyanhein/creating-thumbnail-photo-for-s3-using-lambda-aws/blob/master/Screenshot%20(77).png)
  
  
### 3. Create folder for deployment and inside that folder create another folder called node_modules and run the following command
##### npm install async gm

### 4. Then copy CreateThumbnail.js nodejs file to the root folder
https://github.com/waiyanhein/creating-thumbnail-photo-for-s3-using-lambda-aws/blob/master/CreateThumbnail.js 

### 5. Then create a lambda function. Then add s3 trigger with the configuration required (role previously created, s3 bucket). Zip the deployment package folder and upload it. Then configure the handler. It should look like this.
![picture alt](https://github.com/waiyanhein/creating-thumbnail-photo-for-s3-using-lambda-aws/blob/master/Screenshot%20(78).png)

### 6. Then creat a test function with the policy modified in the hightlighted fields as follow with your credentials. Only the hightlighted areas needs to be  changed. NOTE: file must be already uploaded in the s3 bucket.
![picture alt](https://github.com/waiyanhein/creating-thumbnail-photo-for-s3-using-lambda-aws/blob/master/Screenshot%20(79).png)


##### Then trigger the test function and the thumbnail should be created in the <name>resized bucket. Good luck!

  
