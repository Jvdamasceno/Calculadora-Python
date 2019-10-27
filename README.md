# Calculadora-Python
# coding=utf-8

# Comprimenta o Usuario
print('***********Olá , Seja Bem Vindo***********')

# Multiplica -- por 21
print('--' * 21)

# Solicita o nome do Usuario
nome = input(str('Digite seu Nome :'))

# Solicita o Usuario uma Opção e o Chama pelo nome
print(f"Escolha uma Opção {nome} :")

# Loop para menu de Opções
while True:
    menu = int(input("Digite 1 para soma: \nDigite 2 para Multiplicar: \nDigite 3 para Subtrair: " +
                     "\nDigite 4 para dividir: \nDigite 5 para tirar media: \nDigite 6 para obter a tabuada:"+
                     "\nOpção escolhida:"))
    print("----------------------------------------------------")
#Estrutura Condicional
    if menu == 1:
        # Função SOMA
        def soma(a, b):
            try:
                return float(a) + float(b)
            except ValueError as err:
                return f" Ocorreu um problema, digite um numero: {err}"


        soma1 = input("Digite o valor para soma :")
        soma2 = input("Digite o valor para soma :")

        print(f"{soma(soma1, soma2)}")
        break

#Estrutura condicional
    if menu == 2:
        # Função  MULTIPLICAÇÂO
        def multi(a, b):
            try:
                return float(a) * float(b)
            except ValueError as err:
                return f"Ocorreu um problema, digite um numero: {err}"


        multi1 = input("Digite o valor para Multiplicar :")
        multi2 = input("Digite o valor para Multiplicar :")

        print(f" {multi(multi1, multi2)}")
        break

#Estrutura condicional
    if menu == 3:
        # Função  SUBTRAIR
        def subtrair(a, b):
            try:
                return float(a) - float(b)
            except ValueError as err:
                return f"Ocorreu um problema, digite um numero: {err}"


        sub1 = input("Digite o valor para Subtrair :")
        sub2 = input("Digite o valor para Subtrair :")

        print(f"{subtrair(sub1, sub2)}")
        break

#Estrutura condicional
    if menu == 4:
        # Função DIVIDIR
        def dividir(a, b):
            try:
                return float(a) / float(b)
            except (ValueError, ZeroDivisionError) as err:
                return f" Ocorreu um problema, digite um numero: {err}"


        dividir1 = input("Digite o valor para dividir :")
        dividir2 = input("Digite o valor para dividir:")

        print(f"{dividir(dividir1, dividir2)}")
        break
#-----------------------------------------------------------------------------------------------------------------------
    #Estrutura Condicional
    if menu == 5:
        #Simulação de notas
        media = 0
        listaN = []
        c = 0
        notas = 0
        try:
            c = int(input("Digite  quantas notas Voce quer simular :"))
        except ValueError:
            print("Ocorreu um erro, por favor digite um numero inteiro")
        for x in range(c):
            try:
                notas = float(input("Digite um valor:"))
            except ValueError:
                print("Ocorreu um erro, por favor digite um numero inteiro")
                break
            listaN.append(notas)
            soma = (sum(listaN))
            media = soma / c
            media = round(media, 2)
        print(f"A Media foi: {media}")
        break
    # Estrutura Condicional
    if menu == 6:
        #Tabuada
        num = int(input("Digite um numero para obter a tabuada:"))
        calculadora = 0
        for i in range(1, 11):
            calculadora = num * i
            print(num, "x", i, "=", calculadora)
        break
