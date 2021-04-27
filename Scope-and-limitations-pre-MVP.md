This article describes the shortcuts and limits to the previously defined MVP needed for the first release and attempts to eliminate implementation of both business logic and front end design for several features and behaviors.

## Postponed 
The following need not be implemented

* Scheduling and display of schedules in offer view. 
* Limited uses and display and handling of limits, including information, activation logic and warnings.
* use_expire, the time for which an activated offer is valid, does not need to be added to the offer table or implemented in designs.
* expiration information on offer view. We do not need to display the flag that says an offer is about to expire in the offer view.

In effect, the only conditions for activating an offer is that the user is authenticated and has a valid subscription. 

* Bookmarks, including offer menu entry, custom page and action on offer view.
* History, including offer menu entry, and custom page.
* Search menu. The search menu is meant to display suggested search strings depending on input but now it instead hastily displays matching offers. This is fine but clicking the search field should display the offer menu until input begins (see below).
* Display supported organisation in account view. While we want to store the connection, we do not need to display it.


## Required
The following must be implemented
* The optional www_string needs to be added to the offer table and displayed in the offer view if defined for the offer.   
[[https://github.com/Sporthyra/guldkortet-app/wiki/Offer#additional-content]]
* The optional phone_string needs to be added to the offer table and displayed in the offer view if defined for the offer.  
[[https://github.com/Sporthyra/guldkortet-app/wiki/Offer#additional-content]]
* The cooldownTimer, which defines how often an offer can be used, is not added to the offer table yet does not need to be. Instead the gloabl default cooldown should be 0, meaning offer use spamming is allowed.
* The optional coupon_code needs to be added to the offer table and be displayed in the activated offer if defined.
* The offers menu  
[[https://github.com/Sporthyra/guldkortet-app/wiki/Offers-menu]]  
With the search history and limited to the following custom pages:
  * New offers (also start page when onboarding is completed)
  * Expiring offers   
* Brand block in offer view
[[https://github.com/Sporthyra/guldkortet-app/wiki/Offer#brand]]

## Nice-to-have
* Brand search, custom page for offers of a specific brand  
[[https://github.com/Sporthyra/guldkortet-app/wiki/Offers-from-brand]]
* More offers like this
[[https://github.com/Sporthyra/guldkortet-app/wiki/Offer#more-offers]]
