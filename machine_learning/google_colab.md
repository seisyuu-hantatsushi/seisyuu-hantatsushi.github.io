# Google Colab
## COCODatasetのGoogle DriverへのDownloadの仕方.
```
import os
from google.colab import drive
drive.mount('/content/drive')
os.chdir('/content/drive/MyDrive/Cocodataset')
!wget http://images.cocodataset.org/zips/train2017.zip
```
