# Sistema-de-adivinhar-o-numeros
from random import rand
print('Adivinhe o numero de 1 a 3 ou morra')
vida = 5
rodada = 1
while vida > 0:
    print(40*'-')
    print(f'Rodada: {rodada}')
    print(f'Vida: {vida}')
    print(40*'-')
    sorteio = randint(1, 3)
    sugestao = int(input('Sugestão, sua vida depende disso: '))
    if sugestao > 3:
        print('Ta querendo da uma de espertinho? pois perderá duas vidas pela gracinha')
        vida -= 2
    
    if sugestao == 0:
        print(80*'_')
        print('você tentou burlar o sistema usando "0" e pegará com a vida por isso')
        print(80*'_')
        break
    if sugestao == sorteio:
        vida += 1
    else:
        vida -= 1
    if vida == 0:
        break
    rodada += 1

print(20*'-')
print(f'Sobreviveu a {rodada} rodadas e morreu, tarde demais para tentar novamente...')
