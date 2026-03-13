# Create a Singly Linked List and display elements

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def create(self):
        n = int(input("Enter number of nodes: "))
        
        for i in range(n):
            value = int(input("Enter value: "))
            new_node = Node(value)

            if self.head is None:
                self.head = new_node
            else:
                temp = self.head
                while temp.next:
                    temp = temp.next
                temp.next = new_node

    def display(self):
        temp = self.head
        print("Linked List elements:")
        while temp:
            print(temp.data, end=" -> ")
            temp = temp.next
        print("None")

ll = LinkedList()
ll.create()
ll.display()# Data-structure-practical-program-30
