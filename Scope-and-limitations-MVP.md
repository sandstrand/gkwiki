# General description
The MVP release offers a plattform to replace the current one and offers solutions to the immediate problems in the current application. 

Some features are postponed because we do not have enough user intelligence to design them.
Some features are postpone due to limitations in time, where the complexity and value have been taken into consideration. 

## Scope
The following statements can be made about the release

### Overall Hierarchy
* Brands have
  * Companies 
    * Stores have
      * Region
      * Offers have
        * Categories

A brand can consist of different companies, like franchises, but we front the brand.
A company can have different stores in different locations, even different regions.
An offer could be made available on any subset of stores for a brand.

### Any number of regions/citys can be added to the system.
* A user can only view offers from one region at a time. 
* New users must select a region or city during the onboarding process before browsing offers.
* Online only offers can be added which would be indexed for all regions

### What we list are offers. 
Regardless of how the user traverses the different ways of finding offers, we always list offers, not companies, not categories, even though these are used in the search process.

### New users go through an onboarding process where 
* They are primed them for allowing usage of their phones location data and push messages. 
* They are prompted but not required to create an account. 
* They are prompted but not required to create subscription

### Offers and can be planned
An editor can predefine when an offer should be published and unpublished. 
### Users have control over their account:
On account creation the user provides os with the information needed to gain access to an account if they switch phone, switch phone numer, or switch mail. 
Users that have not logged in are prompted to do so when attempting to use an offer

### Users have an overview of their subscription
* Users can create subscriptions with different imperatives: Create, Extend, Renew.
* Logged in users that do not have a valid subscription prompted to create one when attempting to use an offer.

## Roadmap

### QR code generation
The feature is left out of the MVP.

### Helpdesk and support
While it is identified that a way for users to rate or report problems with offers, no such communication is implemented due to time restraints and lack of support strategy.

### Swish payment
Due to delays in access to the documentation and developer settings, the feature is postponed.

### Maps
While we implement a service for maps and locations, and use this to determine users region and distance to different stores, we do not implement visual maps due to the complexity and time required to do so.

### Push notifications
While we implement a service for push notifications, and gather enough data about users and their preferences to tailor these, we do not have any scripted push messages due to lack of user intelligence and user communication strategy.
 
### User profiles
While track all interactions users have with offers (list, view, use, bookmark etc.), we do not attempt to create any user preference profiles on this data due to lack of user intelligence.

### Editorial content
While the system will offer possibilities to create custom lists of offers, even based tags or even on profiles, and present these with proper content, which would be appropriate for things like 'Father's day' or 'First day of school' we will not implement any complex queries apart form those based on user bookmarks and offer's publish start and end date.

We will for example not have 'Recommended offers' or 'Popular this week' etc, due to time restraints and lack of user intelligence and strategy for such lists.
