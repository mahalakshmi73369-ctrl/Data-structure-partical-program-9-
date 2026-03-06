# Data-structure-partical-program-9-
cart=[]

while True:
    print "1.Add 2.Remove 3.Bill 4.Exit"
    ch=input("Choice: ")

    if ch==1:
        name=raw_input("Item: ")
        price=input("Price: ")
        qty=input("Qty: ")
        cart.append([name,price,qty])

    elif ch==2:
        name=raw_input("Remove item: ")
        for i in cart:
            if i[0]==name:
                cart.remove(i)

    elif ch==3:
        total=0
        for i in cart:
            cost=i[1]*i[2]
            total+=cost
            print i[0],cost
        print "Total =",total

    else:
        break
