The create subscription form is displayed during onboarding and under the account page for authenticated users. The form is the starting point of the subscription process and launches a number of other pages, all of which are declared as common forms, since their content is non-contextual.

When a subscription is successfully created, depending on context, a feedback message might be returned. Feedback messages are defined in the documentation for each context.

Contexts:
* [[Create subscription]]
* [[Onboarding: Create subscription]] 

## Content
* Common component: [[New subscription information]]
* String: `The price for a 12 months subscription is [amount]kr. | Du betalar [amount]kr för 12 måndader.`
* Input 
  * Type: Single select
  * Options:
    * String: `Pay with Swish | Betala med Swish` > [[Swish transaction form]]
    * String: `Pay with credit card | Betala med kort` > [[Credit card transaction form]]
    * String: `I have an activation code | Använd aktiveringskod` > [[Activation transaction form]]
* Button
  * String: `Continue | Fortsätt`
  * Action: Redirects to form according to selection above.

