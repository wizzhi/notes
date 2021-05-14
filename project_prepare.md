## table of user

id   | login | password | email | we_chat | phone | location  | since | pid 
---  | ----- | -------- | ----- | ------- | ----- | --------  | ----- | ---- 
auto |       |          |       |         |       | city?     | date  | ref  


## table of person

pid  | name    | aka     | icon | ref  | dad  | mom  | rank | birth | death 
---- | ----    | --------| ---- | ---- | ---- | ---- | ---- | ----  | ----  
auto | varchar | varchar | id   | id   | id   | id   | \#   | date  | date  


## table of tree

 id   | name  | owner | ref_tree | old_pid | new_pid
------|-------| ------|----------| ------- |------------
 001  | xxx   | uid   |          |         | `(1,2,3)`
 007  | yyy   | uid   |   001    | `(2,3)` | `(8,9,10,11)`
 009  | zzz   | uid   |   001    | `(3)`   | `(0,18)`

The example of 007 is only good for the case of big ref_tree with small list in new_pid.
To avoid recursive query, maybe only allow one level ref? In this case, when there is a update happen on a tree with ref already, we can
1. Always track back to the root tree.
2. Another process to optimize the data structure by: find the common update among all patchse and create a new root leve tree as reference. 
(Then, ref_treee would not have any biz meanning, it bacome a pure technical optimization measure. 
Would the ref key in person level sufficent to perserv all the relations???)

the record of 009 is for remove node 3 while add node 18.
