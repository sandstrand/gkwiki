
# Standard header
The header for the application is displayed as sticky at the top of the screen and consists of the following elements:

## Back navigation
Contextual back navigation is provided when the user is navigating through some processes. Whether or not a has a back link and where it leads is declared on each page template in this documentation.

In some contexts the entire header is replaced by a back navigation, to indicate that the user is in the middle of a process which needs to be actively completed or cancelled.

The backlink consists of
* Icon: `fas fa-arrow-circle-left`
* (Context-dependent) String: `Back | Tillbaka`

## Search
The whole header, apart from the account icon and back-link, is a clickable area which launches the [[Offers menu]]. The menu is an overlay on whatever page the user is on and can be closed to return to the previous content. In some context the search field is hidden from the header.

When entering the 'offers menu' the cursor sets focus on the search input field in the header and shows the OS keyboard is displayed. 

Starting to type string in the search input switches the menu content from offers menu to [[Search menu]]. Once one or more characters have been entered an icon/link to clear the search field is displayed next to the input field, which clears the search string and returns to the offer menu.

When performing a search through the header the searched string replaces the 'Find offer' text in the header. The string remains there as long as the user is browsing trough the results: [[Search result]] > [[Offer]]. It is cleared by navigating away from the result; going to [[Account]] or by going [[Offers from brand]]. Clicking the header again in this state launches the search menu and places the cursor at the end of the input, and lets the user tweak or clear the searched string.

Both menus changes the search icon to a back icon, which closes the overlay.   
Both menus start with the string `Search offers, products and companies | Sök Sök erbjudanden, företag, produkter och tjänster` before any titles or content.
Both menus are scrollable if the content dictates that it must be.

The find offers input field contains the icon `fas fa-search`.

## Account
A link to the [[Account]] page. 
* Link
  * Icon: `fas fa-user-circle`
  * Action: Redirects to [[Account]] page.

# Limited header
During onboarding the header is not displayed and the user can only traverse through the onboarding process. Once the user completes, or cancels, the onboarding process the header is displayed.

# Title
Not all pages have titles. The title content, if any, is declared on each page template in this documentation.

# Onboarding steps
During onboarding a progress indicator is displayed next to the title, which corresponds to the step in the title.

* Completed step: Icon: `fas fa-check`
* Current step: Number
* Next, following steps: Number (alt. colors)

# Messages
[[Feedback and errors]] are displayed after the header and before the content, where applicable.