# Create private repository in ECR

![img.png](Asset/img.png)

Go to the project folder and run the commands:
- docker build -t my_demo_app .
- docker tag my_demo_app:latest 790854961075.dkr.ecr.us-east-1.amazonaws.com/my_demo_app:1.0
- docker push 790854961075.dkr.ecr.us-east-1.amazonaws.com/my_demo_app:1.0

then we have the app image in the ECR.
![img.png](Asset/img1.png)


Change the program and generate the 1.1 version. In the server.js, the MongoDB connection string should be "mongodb://admin:password@mongodb"
- docker build -t my_demo_app:1.1 .
- docker tag my_demo_app:1.1 790854961075.dkr.ecr.us-east-1.amazonaws.com/my_demo_app:1.1
- docker push 790854961075.dkr.ecr.us-east-1.amazonaws.com/my_demo_app:1.1
![img.png](Asset/img3.png)

check the result in http://localhost:3000




