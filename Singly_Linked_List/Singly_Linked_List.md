## Singly Linked List Pseuedocode

## Push

- This function should accept a value
- Create a new node using the value passed to the function
- If there is no head property on the list, set the head and tail to be the newly created node
- Otherwise set the next property on the tail to be the new node and set the tail property on the list to be the newly created node
- Increment the length by one
- return list

## Pop

- If there are no nodes in the list, return undefined
- Loop through the list until you reach the tail
- Set the next property of the 2nd to last node to be null
- Set the tail to be the second to last node
- Decrement the length of the list by 1
- Return the value of removed node
- \*\*Edge Case - if this.length === 0 head and tail are null;

## Shift

- If there are no nodes/no head, return undefined
- Store the current head property in a variable
- Set the head property to be the current head's next property
- Decrement the length by 1
- Return the value of the node removed

## Unshift

- This function should accept a value
- Create a new node using the value passed to the function
- If there is no head property on the list, set the head and tail to be newly created node
- Otherwise set the newly created node's next property to be the current head property on the list
- Set the head property on the list to be that newly created node
- Increment the length of the list by 1
- Return the linked list

## Get

- This function should accept an index
- If the index is less than zero or greater than or equal to the length of the list, return null
- Loop through the list until you reach the index and return the node at that specific index

## Set

- This function should accept a value and an index
- Use your get function to find specific node
- If node is not found, return false
- If node is found, set the value of that node to be the value passed to the function and return true

## Insert

- If the index is less than zero or greater than the length, return false
- If the index is the same as the length, push a new node to the end of the list
- If the index is 0, unshift a new node to the start of the list
- Otherwise, using the get method, access the node at the index minus 1
- Set the next property on that node to be the new node
- Set the next property on the new node to be the previous next
- Increment the length
- Return true

## Remove

- If the index is less than zero or greater thn the length, return undefined
- If the index is the same as the length minus 1, pop
- If the index is 0, shift
- Otherwise, using the get method, access the node at the index minus 1
- Set the next property on that node to be the next of the next node
- Decrement the length
- Return the value of the node removed

## Reverse

- Swap the head and tail
- Create a variable called next
- Create a variable called prev
- Create a variable called node and initialize it to the head property
- Loop through the list
- Set next to be the next property on whatever node is
- Set the next property on the node to be whatever prev is
- Set prev to be the value of the node variable
- Set the node variable to be the value of the next variable
