## table of user

id   | login | password | email | we_chat | phone | location  | since | pid 
---  | ----- | -------- | ----- | ------- | ----- | --------  | ----- | ---- 
auto |       |          |       |         |       | city?     | date  | ref  


## table of person

pid  | name         |  aka         | icon |   sex  | ref  | dad  | mom  | rank | birth | death 
---- |--------------|--------------| ---- |--------| ---- | ---- | ---- | ---- | ----  | ----  
auto | nvarchar(70) | nvarchar(40) | id   | 0,1,2,9| id   | id   | id   | \#   | date  | date  


## table of tree

 id   | name           | owner | ref_tree | pid
------|----------------|-------|----------| -----
 auto | nvarchar(40)   | uid   |   id     | varchar(9999) - accommodate thousands of nodes.
 001  | xxx            | uid   |          | `(1,2,3)`
 007  | yyy            | uid   |   001    | `(1,2,5,6)`
 009  | zzz            | uid   |   001    | 

* pid is the node list of current tree.
* empty list means direct copy of ref_tree, or nothing added if no ref_tree exists.
