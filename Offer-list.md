# Offer lists
A list of offers in accordance with a given query. The query is defined by the page or component where the list is displayed but always 
adhere to the following conditions and restrictions:

## General criteria
* Only offers that are published are listed, regardless of other conditions
* Only offers that are connected to a store which in turn is connected to the same region as the users `last_region` are displayed **_or_** offers which have the virtual flag set, meaning all offers that are 'virtual' are displayed in all regions. When creating an offer, the virtual flag will imply that no stores should be added.

**Any time an offer is displayed in a list an `offer_interaction` of the type `list` is created.**
# Offer list component

## Content

The entire offer card is a link to the single offer view for the offer.

* Symbol: [offer.symbol]
* Header: [offer.title]

### Schedule

* Common component [[Offer schedule]] 

### Locations

* ([offer.location] = virtual)
  * Icon: offer_www_string
  * String: [offer.url]

* ([offer.location] = physical)
  * ( Location data is available )  
List is sorted on distance, closest first.   
Only locations within the [offer_category.radius] are listed.  
See [Locations in offer cards: https://drive.google.com/file/d/1IACIIiVFo0SdNGwoE0EnCEz13_-acUVN/view?usp=sharing](https://drive.google.com/file/d/1IACIIiVFo0SdNGwoE0EnCEz13_-acUVN/view?usp=sharing)
    * (For each store)
      * Icon: store_location
      * String: [store.name]
        * ( Location data is available )  
          * (distance is >= 1000m)  
            * String: '[x.x]km' where ex is distance in kilometers with one decimal.  
          * (distance is < 1000m)
            * String: '[x]m' where ex is distance in meters.

  * ( Location data is not available && number of stores = 1)
    * Icon: store_url
    * String: [store.name]

  * ( Location data is not available && number of stores > 1)
    * Icon: store_url
    * String: '[count stores] locations'

### Expiration notice

* (The [offer.publish_end] is less than 2 days from now)
  * Icon: `fas fa-running`
  * String: `Last chance! | Sista chansen!`



