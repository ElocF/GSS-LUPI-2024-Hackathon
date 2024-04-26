 ![cloud](https://github.com/ElocF/GSS-LUPI-2024-Hackathon/blob/main/media/THECLOUD.png?raw=true)


<br>
Now it is time to do a bit of coding; there is a Python package called [boto3](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html) this package was developed by Amazon to access their proprietary S3 cloud storage through Python. **Boto3 is not available in the general Python install included with ArcPro** 
<br>
<br>
If you are on the GTS to use this package, you must switch your Python environment to a clone. I made a specific clone for this hackathon so we can mess around with it; I will post the path to it in the chat. Your Python environment must change within ArcPro for it to take effect elsewhere. 
[Activate an environment](https://pro.arcgis.com/en/pro-app/latest/arcpy/get-started/activate-an-environment.htm)
<br>
<br>
Once you are set up and have assured that you now have boto3, you are almost ready to rock.... almost???? 
<br>
<br>
Hopefully, you have noticed there is another file in here called constants.py. This short script references a file called .env and assigns it as environmental variables on your machine... But where is the .env file!?!?!?! 
<br>
<br>

![gitignore](https://github.com/ElocF/GSS-LUPI-2024-Hackathon/blob/main/media/cJk23n.gif?raw=true)

<br>
In GitHub you can set up a ".gitignore" file, its in the main directory of the repo, this file tells GitHub what to not show, since the keys to the bucket need to be kept a secret I have made GitHub ignore the .env file. I will post the file in the chat, you can download it and put it in your fork in the same folder as the constants.py and it should work!

ooof glad that's over...Take a look at the S3_tool notebook included in this folder; it has a few ways of interacting with S3, but there are plenty more [available](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/s3-examples.html)

For starters, try:
- finding what is stored in the bucket currently
- how to create folders
- upload something and then delete it (make sure you know what you are deleting)

## Warm up's over
There are two objects in the S3 bucket I put in here and here. 
Write a script that:
- takes one object from the S3 bucket
- download it
- perform some manipulation with arcpy on it or select a subset of data, do what you want
- re-name it and put it here XXXX in the bucket
- upload your script back to the GitHub repo
