## table of user

id   | login | password | email | we_chat | phone | location  | created_on | pid 
---  | ----- | -------- | ----- | ------- | ----- | --------  |------------| ---- 
auto |       |          |       |         |       | city?     |   Date()   | ref  


## table of person

pid  | name         |  aka         | icon |   sex  | ref  | dad  | mom  | rank | birth | death 
---- |--------------|--------------| ---- |--------| ---- | ---- | ---- | ---- | ----  | ----  
auto | nvarchar(70) | nvarchar(40) | id   | 0,1,2,9| id   | id   | id   | \#   | date  | date  


## table of tree

 id   | name           | owner | created_on | type  | ref_tree
------|----------------|-------|------------|-------|----------
 auto | nvarchar(40)   | uid   |   Date()   | v,    |   id

* if type == v, find node by ref_tree


## table of tree - person relation

tid | pid
----|-----

