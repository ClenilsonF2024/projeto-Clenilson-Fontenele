def somar(num1, num2):
    return num1 + num2

def subtrair(num1, num2):
    return num1 - num2

def multiplicar(num1, num2):
    return num1 * num2

def dividir(num1, num2):
    if num2 == 0:
        return "Divisão por zero não é permitida!"
    else:
        return num1 / num2

while True:
    print("Selecione a operação:")
    print("1. Somar")
    print("2. Subtrair")
    print("3. Multiplicar")
    print("4. Dividir")
    print("5. Sair")

    escolha = input("Digite sua escolha (1/2/3/4/5): ")

    if escolha in ('1', '2', '3', '4'):
        try:
            num1 = float(input("Digite o primeiro número: "))
            num2 = float(input("Digite o segundo número: "))
        except ValueError:
            print("Entrada inválida. Por favor, digite números.")
            continue

        if escolha == '1':
            print(num1, "+", num2, "=", somar(num1, num2))
        elif escolha == '2':
            print(num1, "-", num2, "=", subtrair(num1, num2))
        elif escolha == '3':
            print(num1, "*", num2, "=", multiplicar(num1, num2))
        elif escolha == '4':
            print(num1, "/", num2, "=", dividir(num1, num2))
    elif escolha == '5':
        break
    else:
        print("Opção inválida. Tente novamente.")
