## search hospital happy path
* greet
  - utter_greet
* search_provider{"facility_type": "hospital", "location": "San Francisco"}
  - action_facility_search
  - slot{"address":"300 Hyde St, San Francisco"}
* thanks
  - utter_goodbye

## search hospital + location
* greet
  - utter_greet
* search_provider{"facility_type": "hospital"}
  - utter_ask_location
* inform{"location":"San Francisco"}
  - action_facility_search
   - slot{"address":"300 Hyde St, San Francisco"}
* thanks
  - utter_goodbye

## create sales order
* greet
  - utter_greet
* create_sales_order
  - utter_create_sales_order
* thanks
  - utter_goodbye

## create purchase order
* greet
  - utter_greet
* create_purchase_order
  - utter_create_purchase_order
* thanks
  - utter_goodbye


## create sales estimation
* greet
  - utter_greet
* create_sales_estimation
  - utter_create_sales_estimation
* thanks
  - utter_goodbye

## update sales estimation
* greet
  - utter_greet
* update_sales_estimation
  - utter_update_sales_estimation
* thanks
  - utter_goodbye

## create delivery challan
* greet
  - utter_greet
* create_delivery_challan
  - utter_create_delivery_challan
* thanks
  - utter_goodbye

## create customer
* greet
  - utter_greet
* create_customer
  - utter_create_customer
* thanks
  - utter_goodbye

## update customer
* greet
  - utter_greet
* update_customer
  - utter_update_customer
* thanks
  - utter_goodbye


## upload sales order
* greet
  - utter_greet
* create_sales_invoice
  - utter_create_sales_invoice
* thanks
  - utter_goodbye


## create sales invoice
* greet
  - utter_greet
* create_purchase_order
  - utter_create_purchase_order
* thanks
  - utter_goodbye

## happy path
* greet
  - utter_greet
* mood_great
  - utter_happy

## sad path 1
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* affirm
  - utter_happy

## sad path 2
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* deny
  - utter_goodbye

## say goodbye
* goodbye
  - utter_goodbye

## bot challenge
* bot_challenge
  - utter_iamabot
