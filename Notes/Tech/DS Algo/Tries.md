Also called [[prefix tree]]
Typically used to store [[strings]]
Each node acts as a prefix of string
Represents a prefix = characters on the path  till the string + value of node
It is an [[Nary tree]] [[tree]] meaning each node can have any given number of children
Root of the tree is an empty string
All descendants of a node have the same prefix
Remember to initialize an empty root before Trie insertion
It might be important to flag whether a proper word exists at a node of it it is just a prefix maybe using a [[boolean]] flag


