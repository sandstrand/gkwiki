# Queries
## User
Searchable by fully matched phone or email
Reached by ID from Subscription

    {
      user(phone: STRING | email: STRING | id: STRING){
        id
        phone  
        email
        last_region {
          name
        }
        subscriptions{            
          id
          created_at
          activation_date
          expiration_date
          source
          organisation{  
            id
            name
            region{
              name
            }
          }
          transaction{
            payment_method
            amount
          }
        }
      }
    }

## Subscription
Reached by id from User, reached by actrivation_code from subscruptions result list

    {
      subscription(activation_code: STRING | id: STRING) { 
        created_at
        activated_date
        expiration_date
        activation_code
        source
        batch{
          id
        }
        organisation{  
          id
          name
          status
          region{
            name
          }
        }
        user {
          id
          email
          phone
          created_at
          updated_at
          last_region {
            name
          }
        }
        transaction{
          payment_method
          amount
        }
      }
    }  
 

## Organisation
Searchable by partially matched name
Reached by organisation search result list, used in assign batch to organistation user case.

    {
      organisation(name: STRING | id: STRING) {
        id
        name
        description
        status
        symbol
        region{
          id
          name
        }
        subscriptions{
          countTotal
          countActivated
        }
        organisation_type {
          id
          name
          description
        }
      }  
    }


## Organisation Type
Reached by organisation result list, for editing organisation_type,
 
    {
      organisation_type{
        id
        name
        description
      }
    }

## Brands
Searchable by partially matched name
Reached by id from Offer

    { 
      brand(id=STRING | name=STRING) {
        id
        name
        symbol
        company{
          id  
          name
          store{
            countTotal
          }
        }
        store{
          id
          type
          name
          adress
          city
          url
          pos_x
          pos_Y
          region{
            id
            name
          }
          company{
            name
          }
        }
        offer{
          id
          publish_start
          publish_end
          type
          amount
          title
          limit
          location
          offer_category{
            name
          }
        }
      }      
    }

## Region
Reached by region result list, for editing a region, for selecting a region for a store.
  
    {
      region(id=STRING) {
        id
        preposition
        name
        zipcode
        status
      }
    }

## Offer
Reached by brand list of offers

    { 
      offer(id=STRING) {
        id
        name
        symbol
        publish_start
        publish_end
        type
        discount_amount
        discount_type
        use_expire
        cooldown
        qr_code
        coupon_code
        www_string
        phone_string
        title
        content
        limit
        offer_category{
          id
          name
        }
        brand {
          id  
          name          
        }
        stores{
          id
          name
          adress
          city
          region{
            id
            name
          }
          company{
            id
            name
          }
        }
        offer_interaction{
          countList
          countView
          countUse
          countBookmark
        }
      }      
    }


## Offer category
Reached by offer category result list
Can the response be formed as a hierarchal list with parents and children?  
Used to select category for offer.

    {
      offer_category(id=STRING) {
        id
        parent
        name
        symbol
        radius
      }
    }

## Store
Reached by id from brand, for editing stores, for adding stores to offers

    { 
      store(id=STRING | brand.id=STRING){
        id
        type
        name
        adress
        city
        pos_x
        pos_y
        company{
          id
          name
          brand{
            id
            name
          }
        }
      }
    }

## Batches
Reached by id from batches result list, by id from user, by id from subscription 

    { 
      subscription_batch(id=STRING){
        id
        organisation_id
        created_at
        subscriptions{
          countTotal
          countActivated
        }
      }
    }
    

# Urgent mutations for testing
All delete mutations should employ soft delete.

## Create, Delete and Update Operations for offer
* name
* symbol
* publish_start
* publish_end 
* type 
* discount_amount
* discount_type
* use_expire 
* cooldown
* coupon_code
* www_string
* phone_string
* title
* content
* limit
* offer_category.id

## Create, Delete and Update operations for offer_schedule
* offer.id
* day
* time_start
* time_end

## Create, Delete and Update operations for store_offer
* store.id
* offer.id

## Create, Delete and Update operations for store
* company.id
* region.id
* name
* address
* city
* pos_x
* pos_y

## Create, Delete and Update operations for comapny
* name

## Create, Delete and Update operations for brand
* name 
* symbol

## Create, Delete and Update operations for offer_category
* parent.id
* name
* symbol
* radius

