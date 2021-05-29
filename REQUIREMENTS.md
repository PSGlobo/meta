# Project Requirements

![Print of the Big Brother Brasil game](https://i.imgur.com/C3vCUW4.png)

## Functional Requirements

### Admins

Administrators can do everything an Analyst does, plus management operations on BBBs, Pools, Participants etc.

- Can create Polls
- Can create Big brother
- Can register brothers
- Can eliminate brothers
- Can register a round:
    - Can give status to a brother:
        - angel
        - leader and immunity
        - monster
        - immunity by angel necklace
        - immunity by event
- Can register admins
- Can register analysts

### Public

Anyone who accesses the page. They don't need to be logged in.

- Can see the brothers in the open Pool.
- Can see the results of the previous Pools.
- Can see the preview of the next Pool to be open, if there's one scheduled.
- Can vote in one of the options of the active Pool.
    - Votes can be done any number of times while the Pool is open.

## Non-Functional Requirements

- The service should be able to handle at least 1,000 req/s.
- The application should only allow humans to vote. (bots shouldn't vote)


## Entities

- Big Brother
- Round
    - has start/end dates 
      - Rounds cannot overlap
- Pool
    - Has start and end datetime.
    - kinds: Elimination or choosing the winner (final)
- Brother
- User
    - Admin
    - Televiewer
    - Data analyst
- Vote

## Possible Extensions

### A new actor: Analysts

People who should have access to internal information of the system, but do not have permission to change the resources.

- Can "visualize data" of current or past Big Brothers
- Can have access to several statistics of the Pools
    - Total votes
    - Votes by Brother
    - Votes per hour

### Brother Pools

Be able to include in the system the pools made by the brothers inside the game.

## Unresolved Questions

- [x] The angel's necklace is associated to an specific Pool or it has an expiration date?
    - is tied to an specific Pool
