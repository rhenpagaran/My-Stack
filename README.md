# My-Stack


class ImStack:
    def __init__(self):
        print "LIST MANIPULATION USING STACK"
        self.items = input("\nEnter a list of strings:")
        self.items = list(self.items)

    def sort(self):
        return sorted(self.items)

    def reverse(self):
        return self.items[::-1]

    def isEmpty(self):
        return self.items == []

    def insert(self,value,item):
        return  self.items.insert(value,item)

    def push(self, item):
        return self.items.append(item)

    def append(self, item):
        return self.items.append(item)

    def pop(self):
        return self.items.pop()

    def peek(self):
        return self.items[len(self.items) - 1]

    def size(self):
        return len(self.items)


if __name__ == "__main__":
    rpg = ImStack()
    def qt():

        rhen = 0
        print ("\n1. SORT THE LIST \n2. REVERSE THE LIST \n3. ADD AN ITEM \n4. INSERT AN ITEM \n5. GET THE SIZE \n6. COUNT THE PALINDROME")
        x = input("\nChoose the action you want: ")
        if x == 1:
            print "SORTED VERSION: ",rpg.sort()
        elif x == 2:
            rhen1 = []
            while rpg.isEmpty() == False:
                rhen1.append(rpg.peek())
                rpg.pop()
            print "REVERSED VERSION:", rhen1
            return 0

        elif x == 3:
            rh = input("\tEnter the word you wanna add: ")
            rpg.push(rh)
            print "\t",rpg.items
        elif x == 4:
            rh = input("\tInsert: ")
            en = input("\tIndex: ")
            rpg.insert(en, rh)
            print "\t",rpg.items
        elif x == 5:
            print "SIZE:",rpg.size()
        elif x == 6:
            while rpg.isEmpty() == False:
                if rpg.peek() == rpg.peek()[::-1]:
                    rhen += 1
                rpg.pop()
            print "TOTAL PALINDROME: ", rhen
            return 0


        return qt()
    qt()
