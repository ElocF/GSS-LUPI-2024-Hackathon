# The CLOUD
![cloud](https://github.com/ElocF/GSS-LUPI-2024-Hackathon/blob/main/media/THECLOUD.png?raw=true)


<br>
Now its time to do a bit of coding, there is a python package called [**boto3**](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html), this package was devleoped by amazon to access their proprietary S3 cloud storage through Python. **Boto3 is not aviable in the general Python install included with ArcPro** 
<br>
<br>
If you are on the GTS in order to use this package you need to switch your python envrionment to a clone, I made a specific clone for this hackathon so we can mess around with it, I will post the path to it in the chat. Your Python envrionment must changed within arcpro for it to take effect elsewhere, 
![gitignore](https://github.com/ElocF/GSS-LUPI-2024-Hackathon/blob/main/media/cJk23n.gif?raw=true)
<br>
<br>
once your are set up and have assured that you now have boto3 you are almost ready to rock.... almost???? 
<br>
<br>
Hopefully you have notied there is another file in here called constants.py. This is a short script that refernces a file called .env and assigns it as envrionment virables on your machine.... But where is the .env file!?!?!?! 
<br>
<br>
![here's gitignore](media/cJk23n.gif)
<br>
In github you can set up a ".gitignore" file, its in the main directory of the repo, this file tells github what to not show, since the keys to the bucket need to be kept a secret I have made github ignore the .env file. I will post the file in the chat, you can download it and put it in your fork in the same folder as the constants.py and it should work!

ooof glad that's over...Take a look at the S3_tool notebook included in this folder, it has a few ways of interacting with S3 but there are plenty more [avaible](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/s3-examples.html)

for starters I would suggest:
- finding what is stored in the bucket currently
- how to create folders
- upload something and then delete it (make sure you know what you are deleting)

## Warm up's over
There are two objects in the S3 bucket I put in here and here. 
write a script that:
- takes one object from the S3 bucket
- download it
- preform some kind of manipultion with arcpy on it or select a subset of data
- re-name it and put it here XXXX in the bucket
- upload your script back to the github repo 
