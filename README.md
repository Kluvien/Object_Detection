# Object Detection
Deteksi Objek kali ini melakukan deteksi terhadap foto dan video yang ada menggunakan yolov7 dan saya akan menggunakan google colab untuk menjalankannya

berikut adalah langkah2 yang harus dilakukan untuk ke google colab nya

# Setting up Colab Notebook

```python
from google.colab import drive
drive.mount('/content/drive')
```

```python
%cd /content/gdrive/MyDrive/
```

```python
!pwd
```

# Create Directories and Clone Repository

```python
import os

if not os.path.isdir("UAS_Deteksi_Objek"):
  os.makedirs("UAS_Deteksi_Objek")
```

```python
%cd UAS_Deteksi_Objek
```

```python
!git clone https://github.com/WongKinYiu/yolov7.git
```


# Download Pre-trained Model

```python
%cd yolov7
```

```python
!wget https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7.pt
```


# Run Object Detection on Image and Video

```python
!pwd
```

```python
!python /content/UAS_Deteksi_Objek/yolov7/detect.py --weights yolov7.pt --conf 0.5 --img-size 640 --source /content/UAS_Deteksi_Objek/yolov7/1.jpeg
```

```python
!python /content/UAS_Deteksi_Objek/yolov7/detect.py --weights yolov7.pt --conf 0.5 --img-size 640 --source /content/UAS_Deteksi_Objek/yolov7/video1.mp4
```
