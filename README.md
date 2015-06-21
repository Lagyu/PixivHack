#Pixiv Hack

##Introduction  
Pixiv Hack is a tool to automatically crawl illustrations filtered by ratings on www.pixiv.net .

##Usage  
1. Browse www.pixiv.net and sign in with your account. Copy the value of cookies:PHPSESSID using the browser debugger (F12)  
2. You can now close the browser and start Pixiv Hack by running:  
	```
	$ python pixiv_hack.py
	```
3. Follow the prompt and enter the PHPSESSID you just copied, the keyword to search with, the minimum ratings of illustrations to filter with, the maximum number of illustrations to download and whether to download manga.  
4. Sit back and relax! The script will do the rest.  
5. After all work is done, you can check out ```author_info.json``` to view the ratings and the illustration IDs of each Pixiv author that is crawled.  
6. All downloadable illustrations are saved in the ```images``` directory.

##Crawl Illustrations by author IDs  
1. Create a ```.json``` file containing a list of Pixiv member IDs of authors. Sample:  
		authors.json
	```
	["2463004", "19351", "2157729"]
	```
	You can also use ```author_info.json``` which is automatically generated by this script using keyword-search mode described above.  
2. Simply run  
	```  
	$ python pixiv_hack.py -a <JSON_file>
	```
3. Follow the prompt and enter PHPSESSID and other required parameters.  
4. Illustraions are saved in the ```image``` directory sorted by author IDs.

##Dependencies  
* requests

Install using:  
```
$ sudo pip install requests
```

##License
See the ```LICENSE.md``` file for license rights and limitations (MIT).
