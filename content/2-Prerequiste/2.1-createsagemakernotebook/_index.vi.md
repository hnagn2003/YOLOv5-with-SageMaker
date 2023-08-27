---
title : "Tạo notebook SageMaker"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 2.1 </b> "
---

1. **Tạo 1 notebook instance**:
- Name: ```ml-inference```
- Type: ```ml.c5.xlarge```

  ![](/static/images/saved/00.png)
  ![](/static/images/saved/000.png)
  ![](/static/images/saved/001.png)
  ![](/static/images/saved/002.png)

- Trong trường Permissions and encryption, ta tạo 1 role cho SageMaker notebook này

  ![](/static/images/saved/003.png)
  ![](/static/images/saved/004.png)
  ![](/static/images/saved/005.png)



2. Đợi 1 lúc cho trạng thái đổi về **InService**, sau đó click - - **Open JupyterLab** để mở SageMaker notebooks
    
    ![](/static/images/saved/006.png)

    
**3. Với jupiter notebook**
    
Ta chọn môi trường Anaconda Python3
    ![](/static/images/saved/007.png)
{{% notice info %}}
Trong Jupiter Notebook, ta viết mã vào các cell và thực hiện tổ hợp phím *Shift+Enter* để thực thi đoạn mã đó
{{% /notice %}}
    ![](/static/images/saved/008.png)
    
4. **Ta đi clone mã nguồn YOLOv5 cho tác vụ suy luận**
    
    ```jsx
    !git clone https://github.com/ultralytics/yolov5
    ```
    
    Sau đó mở thư mục yolov5
    
    ```jsx
    !git clone https://github.com/ultralytics/yolov5
    ```
    
    Cài thư viện yêu cầu và xuất trọng số ra thư mục *saved_model* để thực hiện việc triển khai mô hình
    
    ```jsx
    !pip install -r requirements.txt tensorflow-cpu
    !python export.py --weights yolov5l.pt --include saved_model --nms
    ```
    
    ![](/static/images/saved/009.png)
    
    - Mô hình sẽ được tải thành công
        
        ![](/static/images/saved/009model.png)
        
    - **Từ giờ tất cả đoạn mã của chúng ta sẽ chạy trên notebook này.** 