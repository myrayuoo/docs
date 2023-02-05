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

Data is automatically saved every 5 minutes, but before restarting or shutting down the server we recommend saving it by executing 2x `ssave()`. If you are on localhost you can do it by using `save()` once.
