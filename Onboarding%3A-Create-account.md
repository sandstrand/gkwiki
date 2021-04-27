This is the first page of third phase of the onboarding process where the user is prompted to create an account.

* From route:
  * [[Onboarding: Push disclaimer]]

* Page title: `3. Account | 3. Konto`

## Content
* Content block: `onboarding_create_account`

  `<p>Almost done.</p>`  
  `<p>To use our offers a subscription is needed. You can get one right here or maybe you have an activiation code.</p>`  
  `<p>Either way, let’s start with setting up your account.</p>` 

* Common component: [[Create account form]]  
  _The form launches the standard process for registration/authentication with no special content. The only specifics for this process during onboarding is that the header is limited._  
  Upon registration and/or authentification the user is redirected to [[Onboarding: Create subscription]]

* Link
  * String: `Skip for now | Jag gör det senare`
  * Action: Redirects to [[Onboarding: Cancelled]]