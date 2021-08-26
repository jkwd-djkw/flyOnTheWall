TEST PLAN

  POSITIVE
    1. Add new charger
    2. Get whole list of chargers
    3. Edit specific charger information
    4. Get specific charger
    5. Remove specific charger

  NEGATIVE
    1. GET SPECIFIC: Show error "Not Found" if the item doesn't exist
    2. EDIT: Show error "Not Found" if the item doesn't exist
    3. DELETE: Show error "Not Found" if the item doesn't exist

  VALIDATIONS
    Endpoint ID invalid
      1. CREATE: Show "Endpoint doesn't exist" error if the your_id is not valid
      2. GET ALL: Show "Endpoint doesn't exist" error if the your_id is not valid
      3. EDIT: Show "Endpoint doesn't exist" error if the your_id is not valid
      4. GET SPECIFIC: Show "Endpoint doesn't exist" error if the your_id is not valid
      5. DELETE: Show "Endpoint doesn't exist" error if the your_id is not valid

    Empty payload
      1. CREATE: Show "Unsupported Media Type" if  empty payload sent
      2. EDIT: Show "Unsupported Media Type" if  empty payload sent

    Wrong payload type
      1. CREATE: Show "Unsupported Media Type" if  wrong payload type sent
      2. EDIT: Show "Unsupported Media Type" if  wrong payload type sent

    Missing item_id
      1. EDIT: Show "Method Not Allowed" error if missing item_id in request
      2. DELETE: Show "Method Not Allowed" error if missing item_id in request

    Invalid item_id
      1. EDIT: Show "Bad Request" error if Invalid item id in request
      2. DELETE: Show "Bad Request" error if Invalid item id in request

  PERFORMANCE
    1. CREATE: Respons should be less than 250ms
    2. GET ALL: Respons should be less than 250ms
    3. EDIT: Respons should be less than 250ms
    4. GET SPECIFIC: Respons should be less than 250ms
    5. DELETE: Respons should be less than 250ms
