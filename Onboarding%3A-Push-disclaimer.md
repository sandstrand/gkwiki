This is the third page of the onboarding process (if we do not have access to location data) where the user selects a region.

* From route:
  * [[Onboarding: Select location]]
  * [[Onboarding: Confirm location]]

* Page title: `2. Notifications | 2. Notiser`

## Content
* Content block: `onboarding_push_disclaimer`

  `<p>We would like to show a you push notifications when we find an offer that we think might interrest you so you don’t miss anything.</p>`

  `<p>We promise to restrain ourselves and not flood you with too many great offers.</p>`
 
* Button
  * String: `OK!| OK!`
  * Action: Launch OS dialog to allow push notifications
    * Allow: Redirects [[Onboarding: Create account]]
    * Deny: Redirects [[Onboarding: Create account]]
* Link
  * String: `Not now | Kanske senare`
  * Action: Redirects to [[Onboarding: Create account]]