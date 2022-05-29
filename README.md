# food-ordering-app
food ordering app
lass Restaurant:
    def __init__(self,name,add):
        self.name = name
        self.add = add
        self.menu = dict()
        self.orders = []
        
    def add_menu(self,name,price):
        self.menu.update({name:price})
        
    def print_menu(self):
        for key,value in self.menu.items():
            print(f'{key} ----> {value}')
        
        
        
    def __repr__(self):
        return f'name: {self.name}, Location:{self.add}'

class User:
    def __init__(self,name,add,phone):
        self.name = name
        self.add = add
        self.phone = phone
    def __repr__(self):
        return f'name: {self.name}, Location:{self.add} Phone:{self.phone}'
    
    def print_menu(self,res_name):
        res_name.print_menu()
        
    
    

KFC = Restaurant('KFC','Hyderabad')

print(KFC)

name: KFC, Location:Hyderabad

KFC.add_menu('Chicken Zinger',55)
KFC.add_menu('Chicken Popcorn',45)
KFC.add_menu('Chicken Burger',105)

KFC.print_menu()

Chicken Zinger ----> 55
Chicken Popcorn ----> 45
Chicken Burger ----> 105

pritom = User('Pritom','Assam','323224242')

print(pritom)

name: Pritom, Location:Assam Phone:323224242

pritom.print_menu(KFC)

Chicken Zinger ----> 55
Chicken Popcorn ----> 45
Chicken Burger ----> 105

