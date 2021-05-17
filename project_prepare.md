## table of user

id   | login | password | email | we_chat | phone | location  | since | pid 
---  | ----- | -------- | ----- | ------- | ----- | --------  | ----- | ---- 
auto |       |          |       |         |       | city?     | date  | ref  


## table of person

pid  | name    | aka     | icon | ref  | dad  | mom  | rank | birth | death 
---- | ----    | --------| ---- | ---- | ---- | ---- | ---- | ----  | ----  
auto | varchar | varchar | id   | id   | id   | id   | \#   | date  | date  


## table of tree

 id   | name  | owner | ref_tree | pid
------|-------| ------|----------| -----
 001  | xxx   | uid   |          | `(1,2,3)`
 007  | yyy   | uid   |   001    | `(1,2,5,6)`
 009  | zzz   | uid   |   001    | 

The example of 007 means node 3 be removed while 5,6 be added.
The record of 009 means soft link to 001, if it is a hard link, pid should be populted.
