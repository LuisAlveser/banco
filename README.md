# banco
# banco
saldo=0
limite=500
extrato="Seu saldo é de R$"
numero_saques=0
Limite_saques=3

while True:
    menu="""
[d] Depositar
[s] Sacar
[e] Extrato 
[q] Sair    
=>"""
    opcao = input(menu)
    if opcao=="d":
        valor_deposito=float(input("Digite o valor do deposito:  "))
        saldo=saldo+valor_deposito
    elif opcao=="s":     
        if numero_saques<=Limite_saques: 
         valor_saque=float( input("Digite o valor do saque: "))
         if saldo>=valor_saque and valor_saque<=limite:
            saldo=saldo-valor_saque 
            numero_saques+=1           
         else:   
            print("Saldo insuficiente ou o saque chegou ao limite")
            break
    elif opcao=="e":
     print(saldo)
       break
    elif opcao=="q":
        break
    else:
        print("Operação invalida,por favor selecione uma opcão valida ")# banco
# banco
