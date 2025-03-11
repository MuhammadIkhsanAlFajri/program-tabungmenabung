# program-tabungmenabung

print('SELAMAT DATANG DI ATM')
print('PILIH OPTION: ')
print('1. Cek uang saya')
print('2. Ambil uang saya')
print('3. Tabung uang saya')
print('4. Selesai')

uang_kamu = 200000

while True:
    try:
        option = int(input('Silakan pilih option: '))
    except ValueError:
        print("Input harus berupa angka!")
        continue

    if option == 1:
        print('Uang saya berjumlah Rp', uang_kamu)

    elif option == 2:
        print('Uang saya berjumlah Rp', uang_kamu, ', mau ambil berapa?')
        print('1. Rp100.000')
        print('2. Rp200.000')
        try:
            option2 = int(input('Option: '))
        except ValueError:
            print("Input harus berupa angka!")
            continue

        if option2 == 1:
            if uang_kamu >= 100000:
                uang_kamu -= 100000
                print('Uang kamu sekarang berjumlah Rp', uang_kamu)
            else:
                print('Saldo tidak mencukupi!')
        elif option2 == 2:
            if uang_kamu >= 200000:
                uang_kamu -= 200000
                print('Uang kamu sekarang berjumlah Rp', uang_kamu)
            else:
                print('Saldo tidak mencukupi!')
        else:
            print('Pilihan tidak valid, mohon ulangi lagi!')

    elif option == 3:
        print('Uang saya berjumlah Rp', uang_kamu, ', mau tabung berapa?')
        try:
            option3 = int(input('Masukkan jumlah uang: '))
        except ValueError:
            print("Input harus berupa angka!")
            continue

        if option3 > 0:
            uang_kamu += option3
            print('Jumlah uang kamu sekarang adalah Rp', uang_kamu)
        else:
            print('Jumlah harus lebih dari 0!')

        elif option == 4:
        print('Terima kasih telah menggunakan program ini.')
        break

    else:
        print('Pilihan anda salah, silakan ulangi lagi!!!')
