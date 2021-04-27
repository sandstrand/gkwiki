
## Content
* String: `Enter the confirmation code we sent to your phone to confirm your phone number. | Ange den engångskod vi skickade till din mobiltelefon för att bekräfta.`
* Input 
  * Type: Text
* Button
  * String: `Confirm | Skicka`
  * Action: Submits the code for verification
  * Possible error message: 
    * `Invalid confirmation code.`   
      `Make sure you entered the code correctly`
      
      `Ogiltig kod.`   
      `Dubbelkolla att du matat in rätt kod.`
* Link
  * String: `Send again | Skicka igen`
  * Action: Sends the code again.   
    Refreshes with the following feedback message:
    `Code sent | Kod skickad`