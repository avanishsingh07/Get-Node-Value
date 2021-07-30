# Get-Node-Value
Given a pointer to the head of a linked list and a specific position, determine the data value at that position. Count backwards from the tail node. The tail is at position 0, its parent is at 1 and so on.

def getNode(llist, positionFromTail):
    # Write your code here
    temp1 = llist
    temp2 = llist
    for i in range(positionFromTail):
        temp1 = temp1.next
    
    while temp1.next != None:
        temp1 = temp1.next
        temp2 = temp2.next
    return temp2.data
