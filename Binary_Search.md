# Data_structure_coursera
### Binary Search Tree : Introduction 
##### Usage : Dictionary Search, Data Ranges, Closest Height...
## Local Search Data Structure  
##### Definition : stores a number of elements each with a key coming from an ordered set. 
     Operation : RangeSearch(x, y) : Returns all elements with keys btw x,y
                 Nearest Neighbors(z) : Returns the element with keys on either side of z
Example : 
|1|4|6|7|10|13|15|  
|-|-|---|-|----|--|--|  

RangeSearch(5,12)  

|1|4|*6*|*7*|*10*|13|15|    
|-|-|---|-|----|--|--|  
  
NearestNeighbors(3)

|*1*|*4*|6|7|10|13|15|    
|-|-|---|-|----|--|--|  
  
## Attempts
### 1. Dynamic Data Structure
     Operation : Insert(x) : Adds a element with key x  
                 Delete(x) : Removes the element with key x 
Example : 
|1|4|6|7|10|13|15|  
|-|-|---|-|----|--|--|  

Insert(3) 
|1|3|4|6|7|10|13|15|  
|-|-|-|---|-|----|--|--|  

Delete(10)
|1|3|4|6|7|13|15|  
|-|-|-|---|----|--|--|  

### 2. Hash Table + Linked List
| | | |   |    |  |10|  
|-|-|-|---|----|--|--|  
|4| |7| 6 |    |  | 1|  
|0|1|2| 3 | 4  |5 | 6|  


