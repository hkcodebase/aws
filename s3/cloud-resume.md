# Static Website Hosting on AWS S3

Here I will show you steps to host a resume file on AWS S3  
1. First we need a resume file in html format - [Sample Resume](https://github.com/hkcodebase/cloud-resume-aws/blob/main/web/index.html)
2. Go to main screen of S3 and create a bucket

![](./s3-main-screen.png)

3. Provide bucket name and region in which you want to create bucket

![](create-step-1.png)

4. Keep other options as default, scroll all the way to end and click on create bucket

![](create-step-2.png)

5. Select the bucket you just created

![](create-step-3.png)

6. Now we will add resume file (index.html), Click Upload under Objects tab

![](create-step-4.png)

7. click on Add Files

![](create-step-5.png)

8. Select your resume file from system and click on upload

![](create-step-6.png) 

![](create-step-7.png)

9. Enable Static Website option 
Click on Properties tab
![](create-step-8.png)

Scroll all the way to down
![](create-step-9.png)

Edit Static Website hosting and enable
![](create-step-10.png)

10. Enable Public Access under Permissions Tab
![](create-step-11.png)
![](create-step-12.png)

11. Add Bucket Policy under Permissions Tab
![](create-step-13.png)
![](create-step-14.png)
![](create-step-15.png)
![](create-step-16.png)

12. Copy Url from Properties Tab
![](create-step-17.png)

Resume is available to access in browser
![](create-step-18.png)