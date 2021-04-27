This is the third page of the onboarding process (if we have access to location data) where the user confirms the regions inferred by the user's location.

* From route:
  * [[Onboarding: Location disclaimer]]

* Page title: `1. Location | 1. Plats` 

## Content
* Paragraph: `<p>Looks like you are [REGION.PREPOSITION] [REGION.NAME].<br /> Is this correct?<p>`  
* Button
  * String: `Correct | Det stämmer`
  * Action: Sets the `USER.LAST_REGION.ID`, redirects to [[Onboarding: Push disclaimer]]
* Link
  * String: `Let me select another location | Låt mig välja från lista istället`
  * Action: Redirects to [[Onboarding: Select location]]
