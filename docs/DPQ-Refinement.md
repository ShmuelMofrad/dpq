# DPQ-Refinement

This is DPQ project Refinement.

## Persons:

 - Manager (Jim’s manager)
 - Deliverer (Jim)
 - Premium Clients (ID 1 - 1000)
 - Clients

## Clients

 - Client IDs range of 1 to 20000
 - Client with IDs less than 1000 are premium

## Orders

 - order (client-Id, quantity of donuts)
 - each client can only place one order
 - existing orders cannot be modified
 - existing orders can only be cancelled
 - all orders will be placed in a single queue

## Sorting

 Orders are sorted by:

 - the number of seconds they are in the queue
 - orders from premium customers always have a higher priority 

### question of sorting

 - Orders must be sorted according to the first-in-first-out concept (FIFO) or calculate with secondary sorting by waiting time.

## Plan of deliveries

 - Max cart holds up to 50 donuts
 - every 5 minutes to pickup counter
 - put into cart without skipping, changing, or splitting

## Implementation

 - RESTful interface
 - A web service: 
   - that accepts the orders
   - that provides a list of items to deliver to the pickup counter
 - Endpoints:
   - client (can order) adding items to the queue (two parameters ID, quantity)
   - client to check his queue position + wait time
   - client to cancel an order (parameter client ID)
   - manager to see all entries + wait time
   - deliverer retrieve next delivery in cart