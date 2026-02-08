my_dict = {}
products_name = {'Laptop', 'Smartphone', 'Headphones', 'Keyboard', 'Mouse', 'Monitor', 
 'Printer', 'Tablet', 'Smartwatch', 'External Hard Drive', 'USB Flash Drive', 
 'Webcam', 'Microphone', 'Speakers','Router'}

values = {'Laptop': 25,'Smartphone': 50,'Headphones': 75,'Keyboard': 40,
'Mouse': 60,'Monitor': 15,'Printer': 10,'Tablet': 30,'Smartwatch': 45,
'External Hard Drive': 20,'USB Flash Drive': 100,'Webcam': 35,'Microphone': 28,
'Speakers': 55,'Router': 12}
for name, qty in values.items():
        my_dict[name] = qty
while True:
        print("1: view")
        print("2: add product")
        print("3: update qty")
        print("4: search")
        print("5: delete")
        print("6: exit")
        choice = int(input('enter choice:'))
        if choice == 1:
                print('=== inventry ===')
                for name, qty in my_dict.items():
                        print(f'{name}: {qty}')
                print(f'total items: {len(my_dict)}')
                input('press enter')
        elif choice == 2:
                product = input('product name:')
                qty = int(input('quantity:'))
                if product not in my_dict:
                        my_dict[product] = qty
                        print(f"add {product}: {qty}")
                else:
                        print('product already existed')
                input('press enter')
        elif choice == 3:
                product = input('product name:')
                qty = int(input('quantity:'))
                
                if product in my_dict:
                        my_dict[product] = qty
                        print(f"update {product}: {qty}")
                else:
                        print('product not found')
                input('press enter')
        elif choice == 4:
                product = input('product name:')
                
                if product in my_dict:
                        print(f"product: {my_dict[product]}")
                        print('product name')
                        input('press enter')
        elif choice ==5:
                product = input('delete name:')
                if product in my_dict:
                        del my_dict[product]
                        print(f"delete {product}")
                        print(f'total items: {len(my_dict)}')
                else:
                        print('not found')
                input('press enter')
        elif choice == 6:
                break
