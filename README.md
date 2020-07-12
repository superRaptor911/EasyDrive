# EasyDrive
A very simple python3 script to download / upload files from **google drive** using [pydrive](https://pypi.org/project/PyDrive/).

# How to install

**Install google client api**
```console
pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib
python -m pip install google-api-python-client==1.8.0
```
**Install pydrive**
```console
pip install PyDrive
```
Now you can use `EasyDrive.py` as a module
# Example

```python
import EasyDrive

#initiate Easy Drive
EasyDrive.init()
#Upload a file to your drive and save it in folder images/cats/ (Folder will be created)
EasyDrive.uploadFile("cat.jpg", "images/cats/cat.jpg")
#Download file from drive and save as cat2.jpg
EasyDrive.downloadFile("images/cats/cat.jpg", "cat2.jpg")
#get FILE resource
file = getFile("images/cats/cat.jpg")
#Permanently delete the file from your drive.
file.Delete()
```
