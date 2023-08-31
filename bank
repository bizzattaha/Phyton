
import time

sayac = 1
balance_ahmet = 0
balance_zeynep = 0
while sayac == 1:
    def menu1():   # Login Menusu
        global giris
        print("— Welcome to Bank (v.0.1) —")
        print("1. Login")
        print("2. Exit")
        giris = input("")
    menu1()
    username_ahmet = 'Ahmet'  # Giriş için bilgileri tanımladım
    userpassword_ahmet = 1234
    username_zeynep = 'Zeynep'
    userpassword_zeynep = 4321
    while sayac == 1:
        if int(giris) == 1:   #login menusundeki secenekleri sıraladım(şartları)
            print("Username:")
            login = input("")
            if login == username_ahmet:
                print("Password:")
                password = input("")
                if int(password) == userpassword_ahmet:
                    break
                else:
                    print("Incorrect Password")
            elif login == username_zeynep:
                print("Password:")
                password = input("")
                if int(password) == userpassword_zeynep:
                    break
                else:
                    print("Incorrect Password!")
            else:
                print("Incorrect Username!")
        else:
            print("Good Bye!")
            break
    def menu():   #Ana menu fonksiyon kullanarak yaptım
        global menu_login
        print("Welcome {0} ".format(login))  # Format.login kullanarak giriş yapanın ismini yazdırdım.
        print("Please enter the number of the service")
        print("1. Withdraw Money")
        print("2. Deposit Money")
        print("3. Transfer Money")
        print("4. My Account Information")
        print("5. Logout")
        menu_login = input("")
    menu()
    while sayac == 1:
        if int(menu_login) == 1:   # ana menunun 1. seçeneğindeki şartları belirttim
            withdraw = int(input("Please enter the amount you want to withdraw: $"))
            if login == username_ahmet:
                if withdraw <= balance_ahmet:
                    balance_ahmet -= withdraw
                    print("{}$ withdrawn from your account".format(withdraw))
                    time.sleep(2)
                    menu()
                else:
                    print("You don’t have {}$ in your account".format(withdraw))
            elif login == username_zeynep:
                if withdraw <= balance_zeynep:
                    balance_zeynep -= withdraw
                    print("{}$ withdrawn from your account".format(withdraw))
                    print("Going back to main menu...")
                    time.sleep(2)
                    menu()
                else:
                    print("You don’t have {}$ in your account".format(withdraw))
                    time.sleep(2)
                    menu()
        elif int(menu_login) == 2:  # ana menunun 2. seçeneğindeki şartları belirttim
            deposit = int(input("Please enter the amount you want to drop: $"))
            if login == username_ahmet:
                balance_ahmet += deposit
                print("{}$ added to your account".format(deposit))
                print("Going back to main menu...")
                time.sleep(2)
                menu()
            elif login == username_zeynep:
                balance_zeynep += deposit
                print("{}$ added to your account".format(deposit))
                print("Going back to main menu...")
                time.sleep(2)
                menu()
        elif int(menu_login) == 3:  # ana menunun 3. seçeneğindeki şartları belirttim + fonk kullandım tekrar döngü olması için
            def menu2():
                global menu_transfer ,transfer
                print("1. Go back to main menu")
                print("2. Transfer Again")
                menu_transfer = int(input(">>>"))
                if menu_transfer == 1:
                    menu()
                elif menu_transfer == 2:
                    transfer()
            def transfer():
                global bakiye,newbakiye,balance_ahmet,balance_zeynep
                transfer = int(input("Please enter the amount you want to transfer:"))
                if login == username_ahmet:
                    if transfer <= balance_ahmet:
                        balance_ahmet -= transfer
                        print("The Transfer Is Successful")
                        time.sleep(2)
                        menu2()
                    else:
                        print("Sorry! You don’t have enough money to complete this transaction")
                        time.sleep(2)
                        menu2()
                elif login == username_zeynep:
                    if transfer <= balance_ahmet:
                        balance_zeynep -= transfer
                        print("The Transfer Is Successful")
                        time.sleep(2)
                        menu2()
                    else:
                        print("Sorry! You don’t have enough money to complete this transaction")
                        time.sleep(2)
                        menu2()
                else:
                    print("Try Again!")
            transfer()
        elif int(menu_login) == 4:  # ana menunun 4. seçeneğindeki şartları belirttim / zaman ve kullanıcı bilgilerini format ile gösterdim
            print("—— Bank ——")
            import datetime
            e = datetime.datetime.now()
            print("—%s/%s/%s %s:%s:%s —" % (e.year, e.month, e.day,e.hour,e.minute,e.second))
            print("———————————–")
            print("Your Name: {}".format(login))
            print("Your Password: {}".format(password))
            if login == username_ahmet:
                print("Your Amount : " + str(balance_ahmet))
            elif login == username_zeynep:
                print("Your Amount : " + str(balance_zeynep))
            time.sleep(5)
            menu()
        elif int(menu_login) == 5: # son olarak ana menunun 5. seçeneğine çıkış şartını belirttim
                print("Your account has been logged out!")
                time.sleep(2)
                break








