# 百度云 + split + openssl = A secured cloud storage

I'm going to share how I backup my massive important personal files &gt; 100GB \(like Photos libraries, documents, etc\) into free cloud storage, we're using Baidu Cloud as an example.

The purpose of the cloud backup is to make sure I have a redundant copies of my VERY important files are stored also in cloud.

DON"T trust your local harddrive, it can be damaged very easily 

DON"T trust cloud storages, they can be damaged or OUT OF SERVICE at any time

PLEASE make sure you have at least one copy of your files on local harddrive, at least one copy of your files in cloud.



Let me show your how I backup one of my Photo library \(NAME: iPhotoLib, SIZE: 47.51GB\)

## Steps

### zip it

![](../.gitbook/assets/kapture-2020-03-01-at-12.26.48.gif)

We will have a new file **iPhotoLib.zip** in the same folder of the original file

### encrypt it \[optional\]

If you want to protect your zip files in cloud, I recommend to use command "openssl" tool to encrypt your zip files, the usage:

```text
# openssl ENCRYPT
openssl enc -des-ede3-cbc -in your_file_name.zip -out your_file_name.zip.openssl -k <your_password>

# openssl DECRYPT
openssl enc -des-ede3-cbc -in your_file_name.zip.openssl -out your_file_name.zip -d -k <your_password>
```

### split it \[optional\]

If you met any single file upload size limitation from your cloud provider, you may need to split it to multiple pieces to bypass the upload limitation, let's check the limitation from BAIDU cloud

![The limitation is 4GB for a single uploaded file](../.gitbook/assets/screen-shot-2020-03-01-at-12.09.04-pm.png)

The split command looks like this

```text
# For non-encrypted files
split -b 4000m your_file_name.zip your_file_name.zip.tmp

# For encrypted files
split -b 4000m your_file_name.zip.openssl your_file_name.zip.openssl.tmp
```

### md5sum it

We have to make sure the file's data integrity, so let's calculate the md5sum value from it.

```text
md5 your_file_name.zip > your_file_name.zip.md5
```

### upload it

Upload all the pieces include the md5 file into cloud storage.

![](../.gitbook/assets/image%20%281%29.png)

It will takes ~1day to upload all the files.

MAKE SURE keep your computer awake.



## Ref





