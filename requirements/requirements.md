# Requirements

## Functional Requirements
1. The user should be capable of listing Smart Fridge from different kiosks with its products (search mechanism)
2. The user should be able to participate of a survey after each purchase made with an authenticated user
3. The user should be capable of adding coupons/promotional prices when purchasing (from external device)
4. After each purchase the Inventory should be updated
5. The user should be allowed to write a feedback (when authenticated) to some purchased product
6. The Kitchen should be capable of updating the inventory when the fridges are refilled

## Non Functional Requirements
1. The service has to be highly concurrent. Multiple costumers can try to purchase the same product
2. The core of the system is the food "delivery" itself, which involves transactions (financial included). This means the system has to be reliable and the database ACID compliant
3. The system should provide telemetry from all of its micro services (observability)
