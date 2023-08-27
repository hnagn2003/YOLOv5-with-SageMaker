---
title : "Activate trigger Lambda for input image"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 4.3 </b> "
---

0. **Open Lambda function you have created and create the trigger**

![](/static/images/lambda/trigger1.png)
![](/static/images/lambda/trigger2.png)

Adding a trigger that execute the job when a event comes.

![](/static/images/lambda/trigger3.png)


1. Open the [Buckets](https://console.aws.amazon.com/s3/buckets) page of the Amazon S3 console and choose the bucket you created earlier
    
    ![](/static/images/lambda/trigger5.png)


    
2. Open folder **Yolov5/**
    
    ![](/static/images/lambda/trigger6.png)

    
3. Choose **Upload**, choose **Add file** and upload a random tiny file 
    
    ![](/static/images/lambda/trigger7.png)
    
    Choose **Upload**
    
    ![](/static/images/lambda/trigger8.png)

    
4. To verify correct operation using CloudWatch Logs
    
    - Open the [CloudWatch](https://console.aws.amazon.com/cloudwatch/home) console. Make sure about your Region
    
    - Choose **Logs**, then choose **Log groups**.
    - Choose the log group for your function
        
        ![](/static/images/lambda/trigger10.png)
        
    - Under **Log streams**, choose the most recent log stream.
        
        ![](/static/images/lambda/trigger9.png)
        
    - If your function has been invoked correctly in response to your Amazon S3 trigger, you’ll see the file `001.png` I upload earlier
        
        ![](/static/images/lambda/trigger11.png)
        
