This is the main account page from which, depending on several different things, the user can create an account, authebntiucate an account, create a subscription, and select region.  

* From route: Header menu link

* Page title: `Account | Konto`

## Content

* (If the user is authenticated) 
  * User information
    * Icon and [user.phone]
    * Icon and [user.email]
  * Common component: [[Subscription information]] 

* (If the user is not authenticated)
  * String `You need to have an account and be logged in before you can use any offers or create a subscription | `     
  * Common component: [[Create account form]]
    _The form launches the standard process for creating an account_  
    During the entire process the header is simplified with only back navigation.  
    Upon completion the user is redirected to [[Account]]

* String: `Your are currently watching offers [region.preposition][region.name]. | `
* Button
  * String: `Change city or region | `
  * Action: Launches OS select dialog with all regions listed. Selecting a region updates user.last_region.