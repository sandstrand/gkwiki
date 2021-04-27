The subscription information is a styled block which conveys information about the current subscription date; whether or not there is a subscription, whether or not it has expired, and with a call to action to create a subscription. It is only displayed for authenticated users.

Contexts:
* [[Account]]
* [[Offer]]

## Content
* (A subscription exists and is valid) 
  * String: `Your subscription is valid [YY-MM-DD] | Din prenumeration gäller till [YY-MM-DD]`   
  * Button      
    * String: `Extend subscription | Förläng prenumeration`
    * Action: [[Create subscription]]

* (At least one subscription exists but none are valid)
  * String: `Your subscription expired [YY-MM-DD] | Din prenumeration löpte ut [YY-MM-DD]`
  * Button
    * String: `Renew subscription | Förnya prenumeration`
    * Action: [[Create subscription]]
* (No subscription exists) 
  * String: `You have no active subscription | Du har ingen giltig prenumeration`
  * Button
    * String: `Create subscription | Skapa prenumeration`
    * Action: [[Create subscription]]
