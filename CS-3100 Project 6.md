# CS-3100 Project Multiset Design
## Brodey Morrow
### Introduction
###### I will be designing a player inventory that stores the item names and the item count. This will be built upon a HashTable<string, int>. When the player picks up an item the item will have it's name and the amount stored in a HashTable.  This will allow the inventory to keep track of the items already in the inventory while allowing it to change the amount of a given item being stored as well as adding new items or the removal of a type of item altogether. 
### Design Philosophy
###### The reason I chose to build the player inventory with a HashTable is because I believe a HashTable is the most efficient way of handling player inventories. It can allow for quick access to the items in the table and the ability to manipulate the amount stored in the hash. The client of the multiset in the game itself and the user is the player of the game.    