## table of user

id   | login | password | email | we_chat | phone | location  | created    | pid | modified
---  | ----- | -------- | ----- | ------- | ----- | --------  |------------| ----|---
auto |       |          |       |         |       | city?     |   Date()   | ref | Date()


## table of person

pid  | name         |  aka         | icon |   sex  | ref  | dad  | mom  | rank | birth | death | created | modified
---- |--------------|--------------| ---- |--------| ---- | ---- | ---- | ---- | ----  | ----  | --------|---
auto | nvarchar(70) | nvarchar(40) | id   | 0,1,2,9| id   | id   | id   | \#   | date  | date  | Date()  | Date()


## table of tree

 id   | name           | owner | created    | type  | ref_tree | modified
------|----------------|-------|------------|-------|----------|----
 auto | nvarchar(40)   | uid   |   Date()   | v,    |   id     | Date()

* if type == v, find node by ref_tree


## table of tree - person relation

tid | pid
----|-----

