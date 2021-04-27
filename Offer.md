The offer page template is used display any and all offers.

* Title: None
* The page has a contextual back-button to which ever list or result the user came from.

**Any time an offer is viewd an `offer_interaction` of the type `view` is created.**

## Content

### Title / Description

An offer has two posssible values to display as the written content depending on which attributes are set. The [offer.title] which is used as a title in offer lists, is a fallback for this content if the optional [offer.content] is not set. 

* (The optional [offer.content] is empty/null/not set) 
  * Header: [offer.title]

* (The optional [offer.content] is set) 
  * Content block: [offert.content]. 

### Activation

* (The user is authenticated _and_ has a valid subscription.)  
  * (The offer has an [offer.limit] and number of [offer_interaction] of the type 'use' for the offer and user is equal or greater than the [offer.limit])  
    * Button (disabled)
      * String: `Use this offer |`
    * String: `You have already used this limited offer and cannot use it again. | `  
  * (An [offer.interaction] of type use exists with a timestamp which is within the [offer.cooldown])
    * Button (disabled)
      * String: `Use this offer |`
    * String: `You have recently used this offer and cannot use it again in HH:ii:ss | `
  * (Else)  
    * Button 
      * String: `Use this offer |`
      * Action: Activates offer. See 'Active offer' section

* (The user is not authenticated)  
  * Button (disabled)
    * String: `Use this offer |`
  * String: You need to log in or create an account to use this and [offer.count] other offers. 
  * Button: 
    * String: `Logga in / Create account | Logga in / Skapa konto` 
    * Action: Redirect to [[Account]] 

* (The user is authenticated but does not have a valid subscription)  
  * Button (disabled)
    * String: `Use this offer |`
  * Common component: [[Subscription information]] with appropriate variant ( Create / Renew )

## Active offer
The section is displayed as a modal popup when the offer has been successfully activated. The user can not navigate away from the view without closing the modal. 

**Any time an offer is activated an `offer_interaction` of the type `use` is created.**

When an offer is successfully activated a [offer_interaction] of type 'use' is created.

If the optional [offer.use_expire] is set, the modal is automatically closed when the expiration time has run out.

On app restart (close/crash/powerloss), and if returning to the offer, it behaves as if the modal has been closed.

* Header: [brand name]
* String: [offer.title]

* (The offer has an [offer.limit] and the number of [offer_interaction] of the type 'use' for the offer and user less than the [offer.limit])  
  * String: `You can only use this offer [offer.limit] time(s). The offer will be valid for ([offer.use_expire] as 'mm minutes and ii seconds'). Do you want to use this offer now?`    
  * Button
    * String: `Yes | Japp`
    * Action: The offer is activated, the confirmation dialog is replaced by the standard content below.
  * Button
   * String: `No | Inte nu` 
   * Action: The modal is closed and the offer is not activated.

* ([offer.qr_code] is set)
  * QR code img: A qr code is generated from the [offer.qr_code] string
* ([offer.coupon_code] is set)
  * Content block: [offer.coupon_code]  
An editor is expected to format a string with instructions and the coupon code when creating the offer.

* Button
  * String: `Close | Stäng`
  * Action: Closes the active offer modal

* ([offer.use_expire] is set)
  * String (animated): 'This offer is valid for ([offer.use_expire] as HH:MM:SS or MM:SS depending on use_expire time)'  

## Additional content.
* ([offer.phone_string] is set)
  * Icon: offer_phone_string
  * String: [offer.phone_string]
* ([offer.www_string] is set)
  * Icon: offer_www_string
  * String: [offer.www_string]

## Expiration notice
* (The [offer.publish_end] is less than 2 days from now)
  * Icon: `fas fa-running`
  * String: `Last chance! This offer expires [ Today | Tomorrow ] | Sista chansens! Det här erbjudandet försvinner [ idag | imorgon ]`

## Schedule
* Common component [[Offer schedule]].

## Limits
* ([offer.limit] is set)
  * Icon: offer_limit
  * String: `This offer can only be used _n_ [ time | times ] | `

## Locations

* ([offer.location] = virtual)
    * location info is not displayed. [offer.www_string] is encouraged to be used instead.

* ([offer.location] = physical)
  * ( Location data is available ) - List is sorted on distance, closest first.
  * ( Location data is not available ) - List is sorted [store.name], asc.

  * (For each store)
    * ([offer.location] = physical)
      * Icon: store_location
      * String: [store.name]
      * ( Location data is available )
        * (distance is >= 1000m)
          * String: '[x.x]km' where ex is distance in kilometers with one decimal.
        * (distance is < 1000m)
          * String: '[x]m' where ex is distance in meters. 
## Brand
* Symbol: brand.symbol
* String: brand.name
* Content block: brand.description
* (more than on offer exists for stores of the brand in the current region)
  * Icon: more_from_brand
  * Link
    * String: `More offers from [brand.name] | Fler erbjudanden från [brand.name]`
    * Action: Redirect [[Offers from brand]] for the brand

## More offers
* (More than one offer exists in the same category for stores in the current region)
  * Title: `Other offers like this | Liknande erbjudanden`
  * Common component: [[Offer list]]  
A list of offers in the same category for stores in the current region

  
 

