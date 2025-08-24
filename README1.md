https://projects.100xdevs.com/tracks/Redis/Redis1


for two backend to communicate ---- use PUB SUBS ---- publisher subscriber




Redis is best suited of caching-----

other than hiiting the DB again and again --we can simply cached the data---
------in memory can be done in BE --- but when the real world apps may have distributed BE ----

so that whose has the in-MEMORY data can't share it with other BE ----- 
so here u need to have the distributed Cahcing ---------

which can be done with REDIS---------- all BE can get cached data from REDIS--------

REDIS ---- is in memory DB ---- EC2----
it is not stored on disk ---

if the in memory data goes down or the server goes down then --- it can still recovered by the queue and the snapshot 
which is taken at evry 1 hr and then all the events are seen --- (ex . backpack.exchange) where u see the orders book----

refer --- snapshot_recover image--------



=======INT QS=========
suppose u have user browser and it sends the req to BE then BE gets cached data from REDIS---
and the REDIS is updated after every 10 mins so --- 
tell me --- if in the 10 mins slot ---- if ADMIN updates new track ---like notes --- on 3rd minute---
--then what would u do----
---as the users still get old cached data -----
-----------------SEE  ----INT.PNG

ANS---option 1-----





-----------for queus ---------
BRPOP --- means block the processs ---
ex ----------- BROPOP 0 -means it will block the process at inifinte unitl some action is done------

BRPOP 30 --- means it will block proces unitl 30 secs------



npm init -y
npx tsc -- init 


Install dependencies in express-server
npm i express @types/express redis


Install dependencies in worker
npm i redis