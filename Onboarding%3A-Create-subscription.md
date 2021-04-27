This is the first page of third phase of the onboarding process where the user is prompted to create an account.

* From route:
  * [[Onboarding: Create account]]

* Page title: `4. Subscription | 4. Prenumeration`

## Content
* Content block: `onboarding_create_subscription`

  `<p>Last step, promise.</p>`  
  `<p>Do you have an activation code or would you like to purchase a subscription?</p>`

* Common component: [[Create subscription form]]  
  _The form launches the standard process for creating a subscription with no special content. The only specifics for this process during onboarding is that the header is limited._  
  Upon completion the user is redirected to [[Onboarding: Completed]]

* Link
  * String: `I'll get a subscription later | Hoppa över`
  * Action: Redirects to [[Onboarding: Cancelled]]