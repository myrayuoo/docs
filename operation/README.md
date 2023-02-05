# Operation

## Opening the screen/backend shell

1. SSH into the server
2. Use the commands below
```sh
cd /var/www/ketamine
sudo screen -ls
```
3. Copy the numbers before the dot from the first line
```sh
sudo screen -r [the numbers you just copied]
```
![image](<https://xello.blue/usercontent/kgIXpBrrYv.png>)
![image](<https://xello.blue/usercontent/YrZhOhxgLj.png>)

You now can see traffic and execute code by typing it in. 

## Saving data

Data is **automatically saved** every 5 minutes, but before **restarting** or **shutting down** the server we recommend **saving it by executing 2x** `ssave()`. If you are on **localhost** you can do it by using `save()` once.

## Editing user data

To first edit someones data you need to get the user object.
**Example:**

```py
get_user("[target username]", "username")
get_user("[target uid]", "uid")
#You can get users by username (username), uid (uid), uuid (uuid), discord id (discord) and auth token (token/[no input]) 
```

After you have a user selected you can change their domain settings for example

```py
get_user("[target username]", "username").domain = "user-edit-testing.xello.blue"
```

To get the current value you can use print function without setting any value

```py
print( get_user("[target username]", "username").domain )
#OUTPUT: user-edit-testing.xello.blue
```

## Updating changes

• Web server directory: `/var/www/ketamine`
Before you make any changes you will need to save the data by using 2x `ssave()` on the cloud or just `save()` if you are on localhost. After that you can shutdown the server by using CTRL+C a few times. Upload the changes using FileZilla, WinSCP or any other FTP Client. Start the server by using
```sh
sudo screen python3 api.py
```
