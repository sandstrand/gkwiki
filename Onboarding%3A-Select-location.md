This is the third page of the onboarding process (if we do not have access to location data) where the user selects a region.

* From route:
  * [[Onboarding: Location disclaimer]]
  * [[Onboarding: Confirm location]]

* Page title: `1. Location | 1. Plats`

## Content
* Paragraph: `<p>We are proud to have [OFFERS.COUNT] available to you but we really think you would rather view the offers that are reasonably close to you.</p>`
 
* Select
  * Placeholder: `Select location | Välj plats`
  * Options: Every published region currently in the system.
* Button
  * String: `Continue | Fortsätt`
  * Action: Sets the `[USER.LAST_REGION.ID]`, redirects to [[Onboarding: Push disclaimer]]
