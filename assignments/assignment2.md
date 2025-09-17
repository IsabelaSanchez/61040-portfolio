# Pset1: Reading and Writing Concepts
## Exercise 1: Reading a concept
Notes on GiftRegistration:
- someone creates a shopping list of items
- their friends can see the list and purchase the items
- Note on principle: when a friend buys one item, the item is not available on the gift list anymore. Also recipient can see which items were bought and who bought them.

### Questions
1) Invariants. What are two invariants of the state? (Hint: one is about aggregation/counts of items, and one relates requests and purchases). Say which one is more important and why; identify the action whose design is most affected by it, and say how it preserves it.
**Answer:**
   invariant 1: The owner user should at least add one item to their registry
   invariant 2: At most one purchase for an item
   The most important is the invariant 1, because if there is no item in the registry, actions like removeItem, open, close, purchase, and count won't be able to work.
   Invariant 1 preserves "removeItem" by... You can only remove an Item if it exists
   Invariant 1 preserves "open and close"...
   Invariant 1 preserves "purchase"
   Invariant 1 preserves "count"
3) Fixing an action. Can you identify an action that potentially breaks this important invariant, and say how this might happen? How might this problem be fixed?
4) Inferring behavior. The operational principle describes the typical scenario in which the registry is opened and eventually closed. But a concept specification often allows other scenarios. By reading the specs of the concept actions, say whether a registry can be opened and closed repeatedly. What is a reason to allow this?
5) Registry deletion. There is no action to delete a registry. Would this matter in practice?
6) Queries. What are two common queries likely to be executed against the concept state? (Hint: one is executed by a registry owner, and one by a giver of a gift.)
7) Hiding purchases. A common feature of gift registries is to allow the recipient to choose not to see purchases so that an element of surprise is retained. How would you augment the concept specification to support this?
8) Generic types. The User and Item types are specified as generic parameters. The Item type might be populated by SKU codes, for example. Explain why this is preferable to representing items with their names, descriptions, prices, etc.




