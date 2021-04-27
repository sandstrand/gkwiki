## Content
* Content block: `expiring_offers`   
`<h1>Last chance</h1>`  
`<p>These offers are about to expire, surely you wouldn't want to let them go unsused?</p>`
* [[Offer list]]  
  * Selection: A list of offers that have a `publish_end` attribute, and where the `publish_end` datetime is less than 3 days from now. General criteria applies.
  * Sort: `publish_end`, closest to expiration first. 

* String on empty: `Seems like there are no expiring offers right now. No need to rush then. | ` 

