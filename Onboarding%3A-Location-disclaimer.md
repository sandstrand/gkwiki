This is the second page of the onboarding process where we explain why we want access to the user's location data, and how we use it.
* From route:
  * [[Onboarding: Welcome]]

* Page title: `1. Select location | 1. Plats`
## Content
* Content block: `onboarding_location_disclamer`  

  `<p>To give you the best and most relevant offers we want you to share your location.<p>`  
  `<p>With location data we can tailor an experience that suits you. We only use this information when you browse offers. We do not save your location data.</p>  `  

* Button
  * String: `Share location | Dela min plats`
  * Action: Launces OS dialog for access to location data. 
    * Allow: Redirects to [[Onboarding: Confirm location]] 
    * Deny: Redirects to [[Onboarding: Select location]]
* Link
  * String: `Maybe later | Inte just nu`
  * Action: Redirects to [[Onboarding: Select location]]

**Exception**  
If there is only one region in the system, the step to confirm or select region is skipped, and the one region is set for the user automatically. In this case the next page in the scenario would be [[Onboarding: Push disclaimer]], regardless of the action in this step.