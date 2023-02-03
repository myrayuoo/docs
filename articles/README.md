# Articles
You can find all of them at [xello.blue/a](<https://xello.blue/a>) and are stored in localstorage/news.json


## Structure
- This is the example of what is stored in the database
```json
{
    "title": "The header for the article",
    "id": "Article ID (uuid)",
    "author": "Author (uuid)",
    "views": the number of views (integer),
    "content": "content of the article",
    "spoiler": "The text that will be displayed on 3rd party websites (like discord or twitter) or on dashboard"
  }
```


## Posting an article
You can add an article by using the [admin dashboard](<https://xello.blue/admin>) or our [tool (recommended)](<https://github.com/Xello-Blue/tools/blob/main/post%20article.py>) written in python

### Admin Dashboard
- Go to https://xello.blue/admin and log in
- Enter the api key into the api key slot ![image](<https://xello.blue/usercontent/oXYROQSZZc.png>)
- Scroll down to section called 'Write an article'
- Fill out the information
- Click the 'post' button


### Python Tool
#### Setup
- Download python (idealy 3.10+) if you don't have already
- Download requests library if you don't have already (`python -m pip install requests` or `python3 -m pip install requests`) 
- Create a file called article.content.html
- Create a file called APIKEY and paste the api key into it

#### Usage
- Write an article in article.content.html
- Change the authorUUID to your uuid
- Run the script and enter the needed information
- Afterwards it should be automatically uploaded to the server


# Code Examples

## How to post an article
1. Importing the required libraries 
```py
import json
import requests

#Download using "python -m pip install requests" or "python3 -m pip install requests"
```
2. Set the payload for the request
```py
payload = {
    "authorUUID": "", #Author of the article (uuid)
    "title": "", #The header for the article
    "spoiler": "", #The text that will be displayed on 3rd party websites (like discord or twitter) or on dashboard
    "content": "" #Content of the article
}
```

3. Create a variable for the api key
```py
api_key = "paste the key here"
```

4. Post the request to the server
```py
response = requests.post(f"https://xello.blue/article/upload?key={api_key}")
print(json.loads(response.content))
```
