## Content
* String: `Submit your phone number to start the transaction. You will complete the transaction in the Swish app. | Ange telefonnummer för swish. Du slutför köpet i Swish-appen.`
* Input
  * Type: Phone
  * Default value: The phone associated with the account.
* Button
  * String: `Continue | Fortsätt`
  * Action: Attempts to initiate transaction towards third party service. 
    Redirects to [[Swish transaction pending]] on success.
  * Possible error messages:
    TBD by third party service provider
* Common component: [[Organisation information]]
