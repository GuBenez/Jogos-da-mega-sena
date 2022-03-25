from random import randint
from time import sleep
print("-=" * 15)
print("{:^30}".format("JOGOS DA MEGA"))
print("-=" * 15)
print()
lista = []
jogos = []
tot = 1
pergunta = int(input("Quantos jogos você gostaria de fazer: "))
print()
while tot <= pergunta:
    cont = 0
    while True:
        num = randint(1, 60)
        if num not in lista:
            lista.append(num)
            cont += 1
        if cont >= 6:
            break
    lista.sort()
    jogos.append(lista[:])
    lista.clear()
    tot += 1
print("-=" * 4, f"SORETANDO {pergunta} JOGOS", "-=" * 4)
for i, l in enumerate(jogos):
    print(f"O jogo {i + 1} foi: {l}")
    sleep(1)
print()
print("-=" * 6, "VOLTE SEMPRE", "-=" * 6)
