'''
class Node:
    def __init__(self, data):   # data -> value stored in node
        self.data = data
        self.next = None
'''

def detectCycle(head):
    if head is None:
        return False
    dicti={}
    current=head
    while current:
        if current in dicti:
            return True
        dicti[current]=True
        current=current.next
    return False
