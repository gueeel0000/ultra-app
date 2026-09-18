# ultra-app
Meu código de vários apps juntos em só um, sendo um projeto iniciante buscando melhorar
import os
import random
import time
def limpartexto(): #limpador de texto
	os.system("cls")
def calculadora(): #Calculadora
	while True:
		desejo = input("Deseja prosseguir? Y/N: ").lower()
		if desejo == "y":
			limpartexto()
			operacaocalc = input("Sua operação: ").lower()
			try:
				numerocalc1 = int(input("Seu primeiro número: "))
			except SyntaxError:
				print("Coloque um numero por favor.")
				continue
			try:
				numerocalc2 = int(input("Seu segundo número: "))
			except ValueError:
				print("Coloque um numero por favor.")
				continue

			if operacaocalc in ["+", "mais", "adição"]:
				limpartexto()
				Respostacalc = numerocalc1 + numerocalc2
				print(Respostacalc)

			elif operacaocalc in ["menos", "subtração", "-"]:
				limpartexto()
				Respostacalc = numerocalc1 - numerocalc2
				print(Respostacalc)

			elif operacaocalc in ["x", "*", "vezes", "multiplicação"]:
				limpartexto()
				Respostacalc = numerocalc1 * numerocalc2
				print(Respostacalc)

			elif operacaocalc in ["divisão", ":", "÷", "/", "_"]:
				try:
					limpartexto()
					Respostacalc = numerocalc1 / numerocalc2
					print(Respostacalc)
				except ZeroDivisionError:
					limpartexto()
					print("Não é possivel dividir por zero. Tente novamente.")
					continue
			else:
				limpartexto()
				print("Escreva uma operação valida!")

		elif desejo == "n":
			limpartexto()
			break

		else:
			limpartexto()
			print("Digite Y/N!")
			continue

def jokempo(): #Jokempô
	while True:
		desejo = input("Deseja prosseguir? Y/N: ").lower()
		if desejo == "y":
			jogadajokempo = input("Sua jogada: ").lower()
			jogadaspossiveis = ["pedra", "papel", "tesoura"]
			bot = random.choice(jogadaspossiveis)
			if jogadajokempo not in jogadaspossiveis:
				print("Resposta inválida, tente novamente!")
				continue
			if bot == jogadajokempo:
				print(f"Empate! tambem joguei {bot}")
			elif bot == "pedra" and jogadajokempo == "tesoura":
				print(f"Eu joguei {bot}, então eu ganhei!")
			elif bot == "papel" and jogadajokempo == "pedra":
				print(f"Eu joguei {bot}, então eu ganhei!")
			elif bot == "tesoura" and jogadajokempo == "papel":
				print(f"Eu joguei {bot}, então eu ganhei!")
			else:
				print(f"Eu joguei {bot}, então você ganhou!")
			continue
		elif desejo == "n":
			break
		else:
			print("Opção inválida. Tente novamente.")
			continue

pikachu = {
     "nome": "Pikachu",
     "tipo": "Elétrico",
     "vida": 100,
     "ataque": 50,
     "energia": 100
 }

def pokemon(): #Pokemon
	pikachu = {
     "nome": "Pikachu",
     "tipo": "Elétrico",
     "vida": 100,
     "ataque": 50,
     "energia": 100
}

charmander = {
"nome": "Charmander",
"tipo": "Fogo",
"vida": 100,
"ataque": 50,
"energia": 100
}

bulbasaur = {
"nome": "Bulbasaur",
"tipo": "Planta",
"vida": 100,
"ataque": 50,
"energia": 100
}

squirtle = {
"nome": "Squirtle",
"tipo": "Água",
"vida": 100,
"ataque": 50,
"energia": 100
}

jigglypuff = {
"nome": "Jigglypuff",
"tipo": "Normal",
"vida": 100,
"ataque": 50,
"energia": 100
}

gengar = {
"nome": "Gengar",
"tipo": "Fantasma",
"vida": 100,
"ataque": 50,
"energia": 100
}

snorlax = {
"nome": "Snorlax",
"tipo": "Normal",
"vida": 100,
"ataque": 50,
"energia": 100
}

mewtwo = {
"nome": "Mewtwo",
"tipo": "Psíquico",
"vida": 100,
"ataque": 50,
"energia": 100
}

lucario = {
"nome": "Lucario",
"tipo": "Lutador",
"vida": 100,
"ataque": 50,
"energia": 100
}

eevee = {
"nome": "Eevee",
"tipo": "Normal",
"vida": 100,
"ataque": 50,
"energia": 100
}
pokedex = [pikachu]

bioma = "Inicial"
def limpar_tela():
    os.system("cls")
mp = 0
if mp > 100:
    mp = 100
def mudar_bioma():
    limpar_tela()
    global mp
    if mp < 10:
        print("Você não tem energia suficiente para ir para outro bioma. Espere um pouco.")
        time.sleep(2 )
        return
    while True:
        bioma_ir = random.choice(["Floresta", "Deserto", "Montanha", "Praia", "Cidade", "Inicial"])
        if bioma_ir == bioma:
            continue
        print(f"Você foi para o bioma: {bioma_ir}")
        time.sleep(2)
        mp -= 10
        caminhada = 1
        while caminhada < 10:
            limpar_tela()
            print(f"Você está caminhando... Tempo até o destino: {10 - caminhada} segundos")
            caminhada += 1
            time.sleep(1)
            continue
        limpar_tela()
        print(f"Você chegou ao bioma: {bioma_ir}")
        time.sleep(2)
        limpar_tela()

def curar_pokemons():
    limpar_tela()
    global mp
    if mp < 5:
        print("Você não tem energia suficiente para curar seus pokémons. Espere um pouco.")
        time.sleep(2)
        return
    print("Seus pokémons foram curados!")
    mp -= 5
    time.sleep(1)

def recuperar_energia():
    global mp
    while mp < 100:
        limpar_tela()
        print("Você está recuperando energia.")
        print(f"Sua energia atual é: {mp}")
        mp += 10
        time.sleep(1)
        continue
    limpar_tela()
    print("Sua energia está cheia!")
    time.sleep(2)
    limpar_tela()

def verificar_energia():
    limpar_tela()
    global mp
    print(f"Sua energia atual é: {mp}")
    time.sleep(2)

def caçar_pokemon():
    limpar_tela()
    global mp
    if mp < 20:
        print("Você não tem energia suficiente para caçar pokémons. Carregue um pouco.")
        time.sleep(2)
        limpar_tela()
    else:
        print("Você está caçando pokémons...")
        time.sleep(2)
        chance = random.randint(1, 100)
        if chance <= 75:
            pokemon_encontrado = random.choice([pikachu, charmander, bulbasaur, squirtle, jigglypuff, gengar, snorlax, mewtwo, lucario, eevee])
            limpar_tela()
            desejo_batalha = input(f"Você encontrou um {pokemon_encontrado['nome']}! Deseja batalhar? Y/N: ").lower().strip()
            if desejo_batalha == "y":
                while True:
                    pokemon_jogador_nome = input("Escolha seu pokémon para a batalha: ").lower().strip()
                    pokemon_jogador = None
                    for p in pokedex:
                        if pokemon_jogador_nome == p['nome'].lower():
                            pokemon_jogador = p
                            break
                    if pokemon_jogador is None:
                        print("Você não possui esse pokémon. Tente novamente.")
                        time.sleep(2)
                        continue
                    break
                while pokemon_jogador['vida'] > 0 and pokemon_encontrado['vida'] > 0:
                    limpar_tela()
                    print(f"Seu {pokemon_jogador['nome']} tem {pokemon_jogador['vida']} de vida.")
                    time.sleep(1)
                    print(f"O {pokemon_encontrado['nome']} tem {pokemon_encontrado['vida']} de vida.")
                    time.sleep(1)
                acao_jogador = input("Deseja atacar ou se curar? (1/2): ").lower().strip()
                if acao_jogador == "1":
                    ataque_jogador = random.randint(pokemon_jogador['ataque'] - 10, pokemon_jogador['ataque'] + 10)
                    pokemon_encontrado['vida'] -= ataque_jogador
                    print(f"Você atacou o {pokemon_encontrado['nome']} e causou {ataque_jogador} de dano!")
                    time.sleep(1)
                elif acao_jogador == "2":
                    curar_pokemon_jogador = random.randint(40, 60)
                    print(f"Você curou seu {pokemon_jogador['nome']} e recuperou {curar_pokemon_jogador} de vida!")
                    pokemon_jogador['vida'] += curar_pokemon_jogador
                    time.sleep(1)
                limpar_tela()
                pokemon_encontrado_acao = random.choice(["atacar", "curar"])
                if pokemon_encontrado_acao == "atacar":
                    pokemon_encontrado_ataque = random.randint(pokemon_encontrado['ataque'] - 10, pokemon_encontrado['ataque'] + 10)
                    pokemon_jogador["vida"] -= pokemon_encontrado_ataque
                    print(f"O {pokemon_encontrado['nome']} atacou seu {pokemon_jogador['nome']} e causou {pokemon_encontrado_ataque} de dano!")
                    time.sleep(1)
                elif pokemon_encontrado_acao == "curar":
                    curar_pokemon_encontrado = random.randint(40, 60)
                    print(f"O {pokemon_encontrado['nome']} se curou e recuperou {curar_pokemon_encontrado} de vida!")
                    pokemon_encontrado['vida'] += curar_pokemon_encontrado
                    time.sleep(1)
                if pokemon_encontrado['vida'] <= 0:
                    print(f"Você derrotou o {pokemon_encontrado['nome']}!")
                    desejo_captura = input("Deseja capturar o pokémon? Y/N: ").lower().strip()
                    if desejo_captura == "y":
                        pokedex.append(pokemon_encontrado)
                        print(f"Você capturou o {pokemon_encontrado['nome']}!")
                        time.sleep(2)
                    elif desejo_captura == "n":
                        print(f"Você deixou o {pokemon_encontrado['nome']} ir embora.")
                        time.sleep(2)

def pokemon():
    while True:
        limpar_tela()

        print("O que deseja fazer?")
        print("0. Voltar para escolher aplicativo")
        print("1. Ir para um novo bioma")
        print("2. Caçar pokémons")
        print("3. Recuperar energia")
        print("4. Verificar energia")

        desejo = input("Escolha uma opção (0-4): ").strip()

        if desejo == "0":
            return  # sai de pokemon() e volta ao menu ULTRA APP

        elif desejo == "1":
            mudar_bioma()

        elif desejo == "2":
            caçar_pokemon()

        elif desejo == "3":
            if mp == 100:
                limpar_tela()
                print("Sua energia já está cheia!")
                time.sleep(2)
            else:
                recuperar_energia()

        elif desejo == "4":
            verificar_energia()

        else:
            limpar_tela()
            print("Opção inválida. Tente novamente.")
            time.sleep(1)


while True:
    limpartexto()
    print("============================")
    print("         ULTRA APP")
    print("============================")
    print("Calculadora: 1")
    print("Jokempô: 2")
    print("Pokemon: 3")
    print("Sair: 0")

    app = input("Escolha um aplicativo: ").strip()

    if app == "0":
        limpartexto()
        break
    elif app == "1":
        calculadora()
    elif app == "2":
        jokempo()
    elif app == "3":
        pokemon()
    else:
        print("Resposta inválida. Tente novamente.")
        time.sleep(1)
