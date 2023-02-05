# Tasks
Task is a way to communicate and receive information from a discord bot (taskbot).

## Available tasks

|Task|Args|Description|Output|
|----|----|-----------|------|
| GET-DISCORD-ACCOUNT | Account ID | Returns `discord.User` that you can use to get account name, id and more | discord.User |
| VERIFY-DISCORD-ACCOUNT | Account ID | Gives an account user role on the discord | Boolean | 
| UPDATE-STATS |  | Updates statistics on the discord server | None |

## Structure
- task.task `string` = The task that you want to execute
- task.args `list` = The arguments you are passing to the taskbot
- task.output `any` = The output `NULL: Processing request` `None: Failed/no return` `*: Success) `

## Example
```py
t = task()
t.task = "VERIFY-DISCORD-ACCOUNT"
t.args = [190000000000000000]

while True:
  if t.output != NULL: break
  
print(t.output)
#True: verified
#False: verification failed
```
