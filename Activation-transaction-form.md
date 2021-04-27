## Content
* String: 'Enter the activation code below. | Ange din aktiveringskod.'
* Input
  * Type: Text
  * Placeholder : XXXXX (for the length of the activation codes.)
* Button
  * String: `Activate | Aktivera` 
  * Action: Verifies activation code. Redirects to context on success.
  * Possible error messages:
    * `Invalid activation code.`  
      `Make sure you entered the code correctly.`

      `Felaktig kod.`  
      `Dubbelkolla att du angett rätt kod.`
    * `Invalid activation code.`  
      `This activation code has already been used.`

      `Felaktig kod.`  
      `Den angivna aktivereingskoden har redan använts.`