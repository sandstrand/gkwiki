The search menu is reach by two means:

* By starting to type in the empty search input displayed when accessing [[Offers menu]].
* By clicking the existing search term displayed in the header while viewing a [[Search result]] or an [[Offer]] through search result. 

## Content

### Search
* Link
  * Icon: `fas fa-search`
  * String: `Search for [string] | Sök efter [string]` 
  * Action: Perform a search on the string in the input and redirect to [[Search result]]

### Suggested search strings.  
A list of strings, updating for each keystroke. The pool of suggested strings is populated by:
* The [name] of each brand that has an store in the current region associated with at least one offer
* The [name] of each offer_category that has at least on offer associated with a store in the current region (or offers without region see [[Offer 
list]])

Not that the index above is only for suggested search strings. The indexed value for n actual search is declared by the [[Search result]] page.

Each string is displayed with 
* Link
  * Symbol: The corresponding symbol for the brand or the offer_category.
  * String: The complete matched string suggested string, the whole brand.name or offer_category.name.
  * Action: Populates the search input field with the string. Perform a search and redirect to [[Search result]].
