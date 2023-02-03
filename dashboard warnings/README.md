# Dashboard Warnings
- You are can sometimes see them on the dashboard at the top of the page. [!image](<https://xello.blue/usercontent/ebDqIhglTZ.png>) They indicate some type of warning or announcement, which is determined by the color/severity.
- You can add or remove them in `localstorage/config.json` under `dashboard-warning` 
- Currently there isn't an automated way to add or remove them (may be added in the future)

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
