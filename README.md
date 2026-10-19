while True:
    print("SIMULADOR DE VALE-TRANSPORTE (VT)")
    print ("1 - Simular")
    print ("2 - Resumo")
    print ("3 - Encerrar")
    
    escolha = input("Escolha uma opção: ")

    if escolha == '1' or escolha == 'simular':
        salario = float(input("Digite o salário: R$ "))
        dias = int(input("Dias trabalhados (1 a 26): "))
        conducoes = int(input("Conduções por dia (1 a 8): "))

        print("1 - Ônibus (R$ 5,00)")
        print("2 - Metrô/Trem (R$ 5,40)")
        print("3 - Integração (R$ 8,90)")

        tipo = input("Escolha o transporte: ")

        if tipo == "1":
            tarifa = 5.00
        elif tipo == "2":
            tarifa = 5.40
        elif tipo == "3":
            tarifa = 8.90
        else:
            print("Tipo de transporte inválido!")

        gasto_mes = tarifa * conducoes * dias
        desconto_vt = salario * 0.06

        if gasto_mes > desconto_vt:
            print("Vale a pena pedir VT!")
        elif gasto_mes == desconto_vt:
            print("Tanto faz.")
        else:
            print("Não compensa pedir VT.")

    elif escolha == '2' or escolha == 'resumo':
        print("Exibindo resumo...")
    elif escolha == '3' or escolha == 'encerrar':
        print("Encerrando...")
        break
    else:
        print("Opção de menu inválida!")
