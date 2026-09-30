[1] For the Retail Series Regression Project the following things has been followed:

 The main idea behind the inventory optimization is if the shop has too much unsold products on the shelf then it is overstock problem,
 or they could be facing the problem of understock which means the shop does not have enough stocks of products which are in high demand.

 The following will be explained in steps:
 
 Step1 [Figure out by how much currently demand-supply is messing this up]:
 (a) Historical data: on how many days did Units Sold come close to or exceed Inventory Level? Those are the stockout days.
 (b) On how many days was Inventory Level way higher than what actually sold? Those are the overstock days
 
 Step2 [Understand the demand is for each product]:
 (a) Steady demand: By how much little extra stock (buffer) can be kept, since tomorrow's prediction can be done closely.
 (b) Unpredictable demand: In need of a bigger safety cushion, because prediction cannot be done precisly.

 Since there are features like Store ID which stores the store numbers, we can calculate average sales per store-product combination,
 and how much sales is closer or over the average sales.

 Step3 [Deciding on how much risk of running out the business is willing to accept]:
 (a) If the business wants to avoid the stockouts by 95% of the time, that is considered the service level
 (b) If the business decides to run a higher service level for example; let's say 99%, then the entity is running the risk of overstock problem
 (c) A lower service level (say 90%) means less buffer stock — cheaper, but the enterprise run out more often.

 Step4 [Building a Safety Stock Level]:
 (a) Based on the above Step 2 and Step 3, the products whose demand varies greatly then those products get larger safety stock level
 (b) Again the products whose demand and sale has been consistent with little variability then those products will get the smaller 
     Safety stock level.
     
 The general intuition is around : safety stock = how much the entity want to avoid the stock out * how unpredictable the demand is * 
                                    how long it takes to restock
 There is another factor which involves how fast the business can restock, if a product has larger restock period then requires a larger inventory level
 than the one whose time to restock is overnight.

 Step5 [Set the "reorder point" — when to actually place a new order]:
 The reorder point refers to the level of stock, the moment it reaches the position , the firm has to reorder for the product, because after that buffer stock
 level starts before the new quantities comes.

 reorder point = (expected daily sales × days until restock arrives) + safety cushion.

 Step6 [Deciding on how much to order]:
 Order up to a target level — refill back to a level that covers the next period plus buffer.

 Step7 [Testing rule against history]:
 (a) Pretend you're back in time, day by day, using your new reorder point and order quantity rules instead of what actually happened.
 (b) Simulate: would this rule have prevented the stockouts you found in Step 1? Did it avoid piling up as much excess stock?
 (c) Compare: "Old approach: 12% stockout rate, average overstock of X units. New approach: 3% stockout rate, average overstock of Y units."

 Step8 [Not treating every product the same]:
 (a) Split products into groups — e.g. your best-sellers / highest revenue products vs. your slow-movers.
 (b) Give the important, high-revenue products a tighter, more careful policy (higher service level, since stockouts there hurt more).
 (c) Give low-revenue, low-priority products a looser policy (don't over-invest effort or cushion stock there)

 This shows it is not just running a formula blindly — Applying judgment about where inventory precision actually matters for the business.
