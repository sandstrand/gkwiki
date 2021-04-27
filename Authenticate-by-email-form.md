The form allows for authentication for existing users by email. The form launches a number of other pages, all of which are declared as common forms, since their content is non-contextual.

## Content

* String: `Submit your email address to log in. A code will be sent to you which you can use to log in. | Ange din epostadress. Vi kommer att skicka dig en engångskod som du använder för att logga in.`  
* Input 
  * Type: Email
* Button
  * String: `Continue | Fortsätt`
  * Action: Submits form and redirects to [[2FA email form]]
  * Possible error messages:
    * `We could not find any account with this email address.`  
      `Det finns inget konto med den epostadressen.`
* Link
  * `Use phone number instead | Skicka via SMS istället.`
  * Action: Redirects to [[Authenticate by phone form]]