# Dashboard Warnings
- You are can sometimes see them on the dashboard at the top of the page. They indicate some type of warning or announcement, which is determined by the color/severity.
- You can add or remove them in `localstorage/config.json` under `DASHBOARD.warning` 
- Currently there isn't an automated way to add or remove them (may be added in the future)
- By clicking on the warning you can hide it until the page is refreshed
![image](https://user-images.githubusercontent.com/83588955/216693011-8ba2a4b7-1b97-4620-9cb6-01565a434f25.png)


## Example:
```json
{
  "icon": "triangle-exclamation",
  "content": "This is a warning",
  "level": "3"
}
```

### Icon
- An icon shown with the message
- You can find the available icons [here](<https://fontawesome.com/>)

### Content
- The message of the warning
- Can contain HTML

### Level
- Alert Severity

### Severity Levels
Level | Color   | Severity
------|---------|---------
  0   | Green   | None
  1   | Purple  | Low
  2   | Orange  | Moderate
  3   | Red     | High
