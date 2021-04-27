The form allows for authentication for existing users by phone, and is the default method for authentication. The form launches a number of other pages, all of which are declared as common forms, since their content is non-contextual.

## Content

* String: `Submit your phone number to log in. A code will be sent to your phone by SMS. | Ange ditt mobiltelefonnummer. Vi kommer att skicka en engångskod via SMS som du använder för att logga in.`  
* Input 
  * Type: Phone
* Button
  * String: `Continue | Fortsätt`
  * Action: Submits form and redirects to [[2FA phone form]]
  * Possible error messages:
    * `We could not find any account with this phone number.`  
      `Det finns inget konto med det telefonnumret.`
* Link
  * `Use email instead | Skicka via epost istället.`
  * Action: Redirects to [[Authenticate by email form]]