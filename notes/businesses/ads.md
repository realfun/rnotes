Ads system dissection
---------------------

 * User profile
 * Bids information
 * Match user and bids
 * Storm processing
 * Realtime bidding
 * TODO: more?
 
### User profile
 
 * Identify User(very hard when cross device)
 * Beacon
    - 1x1 pixel, contains page_ref(url) and all bcookie stuff
    - usually client will include a piece of script from ads provider, google/yahoo/bing ads
 * User's implicit interest
    - search log
    - page view
    - social info(TODO: how?)
 * User profile contains attributes bid matches for, like keywords, tags, etc.

### Bids information
  * Some rules that matches attributes of the profile
  * usually stored in relational database

### Match user and bids
  * User went to a page triggers beacon, got user profile, request to load news
  * Based on bidding and amount(TODO: ?how this is calculated)

### Storm processing
  * When a beacon request comes in, url was crawed to get info, added to user profile, then matches current bids
  * TODO: (?not sure? when bids comes in, need to wait for user beacons, for big system the latency should be small)

### Realtime bidding
  * in good old world, brand will contact media directly
  * market drives for maximized profit, so bidding exists
  * media has users, and can build user profiles
  * media want to focus on content, so outsourced the matching to bidding firms, sellable by Cost-Per-Read, Cost-Per-Click, etc.
  * media ads position has many types, video, game, display, etc...
  * brand needs ads design, usually outsourced to big ads firms
  * big ads firms usually looking for bidding firms as it's design is affected by that
  * usually big ads firms give suggestions based on which type of media the ads should go to, design for these media(video, newspaper, etc)
  * big ads firms usually went to resellers of each media type(TODO: ?need more investigate)
  * realtime bidding firm matches both sides, in realtime
  * TODO: how is the architecture?

