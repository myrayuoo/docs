# Badges

## Structure

### Database
- This is an example of what is saved in the database
```json
{
  "icon": "star",                         <- The icon that represents the badge 
  "label": "A badge",                     <- Text that will be shown once you hover over the badge
  "description": "A short description",   <- What does the badge mean
  "color": "00FF00",                      <- Badge color in HEX
  "id": "BADGE"                           <- ID that is stored in user object
}
```

### Object
- This is an example of what is it when its loaded
```py
class badge:
  def __init__(self):
    self.icon = "star"                        # The icon that represents the badge 
    self.label = "A badge"                    # Text that will be shown once you hover over the badge
    self.description = "A short description"  # What does the badge mean
    self.color = "00FF00"                     # Badge color in HEX
    self.id = "BADGE"                         # ID that is stored in user object
``` 

## Adding and removing a badge

### Adding
```py
u = user object
u.add_badge(badge_id)
```

### Removing
```py
u = user object
u.remove_badge(badge_id)
```

## Badge list

|Name|ID|Icon|
|----|--|----|
|Developer|DEVELOPER|code|
|Staff|STAFF|screwdriver-wrench|
|Moderator|MOD|shield-halved|
|Contributor|CONTRIBUTOR|code-merge|
|Beta Tester|BETAUSER|flask-vial|
|Bug Hunter|BUGHUNTER_LVL1|bug|
|Verified User|VERIFIED|award|
|Early User|EARLYUSER|user-astronaut|
|Community Volunteer|COM_VOLUNTEER|seedling|
|Lunar|LUNAR|venus|
