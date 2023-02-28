### Unzip file with python


~~~
from zipfile import ZipFile

filename = 'filename.zip'

with zipfile.ZipFile("/home/ubuntu/%s"%filename, 'r') as zip_ref:
    zip_ref.extractall("/home/ubuntu/")

~~~
