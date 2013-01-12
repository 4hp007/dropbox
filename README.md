dropbox.jar
=======
Upload a list of files to dropbox server based on [dropbox java sdk](https://www.dropbox.com/developers/reference/sdk). 



Setup
====

### Create dropbox app

Create your app in dropbox via [here](https://www.dropbox.com/developers/apps).  Mark down the app key and app secret.


### Get access token pair
        git clone https://github.com/Jintian/dropbox.git
  		cd dropbox
  		mvn clean install
  		mvn exec:java -Dexec.mainClass="com.dengjintian.uploader.GetAccessTokens" -DappKey=yourAppKey -DappSecret=yourAppSecret

A webpage will be opened in your browser and you need to authenticate your app.
After that, you will get the access key and access secret.

![console](http://blog.dengjintian.com/wp-content/uploads/2013/01/Snip20130112_3.png "hi")


### Run and upload file!!!

		java  -DappKey=yourAppKey -DappSecret=yourAppSecret -DaccessKey=yourAccessKey -DaccessSecret=yourAccessSecret -jar target/dropbox.jar xxxx yyyy …
		
*No matter the uploading is finnished or not, the program will terminate in 1 minute by default. You can extend it by* -Dtimeout, e.g. -Dtimeout=5 which means 5minutes. 





