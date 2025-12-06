# CS-3100 Project Multiset Design
## Brodey Morrow
### Introduction
###### I will be designing a player inventory that stores the item names and the item count. This will be built upon a HashTable<string, int>. When the player picks up an item the item will have it's name and the amount stored in a HashTable.  This will allow the inventory to keep track of the items already in the inventory while allowing it to change the amount of a given item being stored as well as adding new items or the removal of a type of item altogether. 
### Design Philosophy
###### The reason I chose to build the player inventory with a HashTable is because I believe a HashTable is the most efficient way of handling player inventories. It can allow for quick access to the items in the table and the ability to manipulate the amount stored in the hash. The client of the multiset in the game itself and the user is the player of the game. 
### Core Operations
######  There are four core operations that a multiset should support. The first operation that the multiset will support is an insert function. It should run at a O(log n) time complexity. When the player picks up an item that item's name is used it's key a hashcode is then generated the item is then stored at the index that corresponds to the hashcode. An edge case would be receiving an item from an npc. The HashTable is being supported because without the operation there would be no way to insert new items. 

#### Pseudo code
```text
DEFINE HashTable AS ARRAY OF BUCKETS called buckets
DEFINE HashTable_size as size_t
Function insert(key,value);
 return true or false
 START
 GET hashcode from key % HashTable_size
 CREATE a bucket containing key and value
 IF hashcode matches an index in buckets
 INSERT bucket into buckets
 RETURN true
 IF hashcode doesn't match any index in buckets 
 RETURN false
 ```  



###### The next operation would be a erase function. This would run at a time complexity of O(log n). When the player either drop an item or expends an item the item will the index that the item in question was in is cleared. An edge case for this operation is if a item is removed for a quest. The underlying data structure supports the operation because without the operation the table would get clogged with expended items. 

###### The next operation is a find function. The way this operation would work in game is with a search bar. If the player types the name of an item into the search bar the HashTable is searched for a key that matches the name entered by the player. It should have a time complexity of O(log n). A possible edge case is when the player searches for an item that is not in the player's inventory. The data structure supports the operation because the HashTable is what stores the inventory items.

###### The last operation is a Traverse function. This function would be used to sort the inventory when ever the player prompts it. It should have a time complexity O(n). A possible edge case is if all of the items in the inventory are the same type. The data structure supports the operation because the HashTable is what stores the inventory items.














### Sources
https://www.geeksforgeeks.org/cpp/multiset-in-cpp-stl/
