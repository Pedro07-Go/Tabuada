# Tabuada
# Um projeto simples utilizando python para o aprendizado da tabuada
import time
import random

o = 0
p = 0

print("Voçê tem 20 segundos para responder o maxímo de contas")

def minha_tarefa_repetitiva():
    global o
    global p

    N1=[1,2,3,4,5,6,7,8,9]
    N2=[1,2,3,4,5,6,7,8,9]

    N_1=random.choice(N1)
    N_2=random.choice(N2)

    resultado = N_1 * N_2

    print(f"{N_1} x {N_2} =")

    x=int(input())
    
    if x == resultado:
        o = o + 1
        print("correto")
    elif x!= resultado:
        p = p + 1
        print("errado")
    print("----------------------")
    print(f"acertos:{o}")
    print(f"erros:{p}")

tempo_total_segundos = 20
intervalo_segundos = 0    

inicio = time.time()

while (time.time() - inicio) < tempo_total_segundos:
    minha_tarefa_repetitiva()
    time.sleep(intervalo_segundos)
    print(f"Tempo decorrido: {time.time() - inicio:.2f}s")

print("ACABOU O TEMPO")
input("pressione enter para finalizar")
