The create account form is displayed during onboarding and on the account page for anonymous users. The form is the starting point of the registration and/or authentication process and launches a number of other pages, all of which are declared as common forms, since their content is non-contextual.

Contexts:
* [[Account]]
* [[Onboarding: Create account]]


## Content
* Input 
  * Type: Phone
  * Label: `Phone number | Mobiltelefonnr`
* Input 
  * Type: Email
  * Label: `Email address | Epostaddress`
* Button
  * String: `Continue | Fortsätt`
  * Action: Submits form and redirects to one of the following on success:
    * [[2FA phone form]]
    * [[2FA email form]]
  * Possible error messages:
    * `Cannot create account`  
      `The phone number and email you supplied cannot be used together. `  
      
      `Kunde inte skapa konto`  
      `Det telfonnrummer och den epostaddress du angivit kan inte kombineras.`
* Link
  * `I already have an account | Jag har redan ett konto`
  * Action: Redirects to [[Authenticate by phone form]]