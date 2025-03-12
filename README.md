saida = ''

# adição
def adicao(num1, num2):
    return num1 + num2

# subtração
def subracao(num1, num2):
    return num1 - num2

# multiplicação
def multiplicacao(num1, num2):
    return num1 * num2

# divisão
def divisao(num1, num2):
    if num2 == 0:
        return "Não foi possível realizar a divisão por 0"
    else:
        return num1 / num2

# Calculadora
def calculadora(num1, num2, operacao):
    if operacao == "+" or operacao.lower() == "adicao":
        resultado = adicao(num1, num2)
    elif operacao == "-" or operacao.lower() == "subtracao":
        resultado = subracao(num1, num2)
    elif operacao == "*" or operacao.lower() == "multiplicacao":
        resultado = multiplicacao(num1, num2)
    elif operacao == "/" or operacao.lower() == "divisao":
        resultado = divisao(num1, num2)
    else:
        resultado = "Operação inválida!"
    
    return resultado

# Controle de execução
while saida.lower() != 'n':
    
    try:
        num1 = float(input("Digite o primeiro número: "))
        num2 = float(input("Digite o segundo número: "))
        operacao = input("Digite a operação (+, -, *, /) ou o nome da operação (adicao, subtracao, multiplicacao, divisao): ")

        resultado = calculadora(num1, num2, operacao)
        
        print(f"Resultado da operação: {resultado}")
        
    except ValueError:
        print("Por favor, digite um número válido!")

    saida = input("Deseja continuar? (S/N): ").strip()

print("Programa encerrado.")
