# Tasks
Task is a way to communicate and receive information from a discord bot (taskbot).

## Available tasks

|Task|Args|Description|
|----|----|-----------|
| GET-DISCORD-ACCOUNT | Account ID | Returns `discord.User` that you can use to get account name, id and more |
| VERIFY-DISCORD-ACCOUNT | Account ID | Gives an account user role on the discord |
| UPDATE-STATS |  | Updates statistics on the discord server |

## Structure
- task.task `string` = The task that you want to execute
- task.args `list` = The arguments you are passing to the taskbot
- task.output `any` = The output `NULL: no output yet` `None: failed` `*: success) `
