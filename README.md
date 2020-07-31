# hashing1
 
This program demonstrates hashing in programming (this one beginning python  )

#creating a class 
class hash:
    #initializing
    def __init__(self):
        self.Max = 100 #to find the hash 
        self.arr = [None for i in range(self.Max)] #list of 100 None 
     #example ["none","none","none".....] 100 times

    #will insert a word or character and will output ascii total number 
    def get_hash(self,key):
        h = 0
        for char in key:
            h += ord(char)
        return  h % self.Max
    #Max will also be used for finding the reminder 
    #adding the value of dictionary in the list example {"key":value} #value is added to the arr of list called hashing to store the value #in computer format         
    def item_to_be_placed_in_hash(self,key,value):
        h = self.get_hash(value)
        self.arr[h] = key
    #to retrieve the value from the array or list 
    def get_the_item_from_array(self,key,value):
        h = self.get_hash(value)
        if key == h:
            return self.arr[key]
        else:
            print("None")


l1 = hash()
j = l1.get_hash("march")
#will print the hashed key
print(j)
l1.item_to_be_placed_in_hash(21,value="march")
#will store 21 in the list of array where the value of key 
m = l1.get_the_item_from_array(j,value="march")
#will retrive the data from the arrary of list 
print(m)