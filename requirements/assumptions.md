# BACKGROUND / ASSUMPTIONS

From what was stated in the transcript we can assume that:

1. Toast already integrates with SF to manage transactions along with products on it contained.

2. It should already exist some customer management service (and an authentication service as well) and this should be already integrated with Toast. In fact if the credit card used to perform the transaction belong to some customer they can align that customer to the purchase. However they currently can't align the customer to the purchase if he/she didn't register a card in his personal account, and they are looking for a way to do it.

3. Toast allows for integrations and a lot of products are available in the market.
   We have to assume that Toast is capable, or it is possible enabling it to send a message/event/notification when a
   purchase is done.
   This message/event/notification should contain all the details, kiosk location, items bought, credit card used (and  
   eventually the email address and or Name and Surname in case the person who declared his own account ... this
   could be a way "for making sure we're basically aligning each potential customer").