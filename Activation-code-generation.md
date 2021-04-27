## Conditions and risks

Determining an appropriate level of security (length of key) for unique keys is dependent on a few parameters:
* _How easy is it to perform a brute force attack with the provided interfaces?_
  * We do not allow for activation attempts in any other interface than the application. These could still be emulated in an environment where 
systematic brute force attacks can be performed.
  * Unique keys without a limited lifecycle are more likely to be brute forced.  
  * Activation attempts require an authorized account.'
* _What are the implications of a key being used by the wrong user?_
  * Guessing an activation code will not give the user access to any sensitive information.
  * We do not really loose money on getting more active users, as long as this is not put into system to circumvent the proper sales channels.
  * Trying to use a key which has already been activated is an unpleasant scenario for the user who rightfully payed for the activation code.

## Suggestions

Activation codes may not need an expiration date, but we could implement a defense against systematic brute force attacks:  

After _x_ failed attempts a cooldown is put in place between attempts, mitigating the effectiveness of brute force attacks. We could also display some instructions for the user to contact customer service for aid, in case a code has been wrongfully used and the user who has rightfully paid is the one repeatedly failing. If we discover systematic attempts we could lock accounts with too many failed attempts.

If a user contacts us and not being able to use a code, and we can verify that the code exists, we can assume the user has payed for it and for some reason it has been activated elsewhere. We loose nothing from creating a new subscription for these customers.

## Generation 

It is projected that there will be up to 100 000 active subscriptions during the coming year, even though not all of these will originate form an activation code.

For readability and usability we should only use characters A-Z and numbers 0-9. letters should not be case-sensitive and we should write and communicate these with capital letters.

The key strength can be calculated as such: 

`[Chance of guessing] = [Number of valid keys] / ([character options] ^ [key length])`

A pool of 100 000 valid codes within a 8 character range, where we use non-case-sensitive letters A-Z and digits 0-9 would give the following:

`1000000 / 36 ^ 8 = 0,0000035% `  

The length of the key could be expanded later.   
Activation codes should not be reused.
