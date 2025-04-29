# -Adivina-el-N-mero-en-PSeInt-
Proceso AdivinaElNumero

	Definir numeroSecreto, intento, numeroUsuario, maxIntentos Como Entero
	Definir gano Como Logico

	numeroSecreto <- Aleatorio(1, 100)
	maxIntentos <- 7
	gano <- Falso

	Escribir "🎯 Bienvenido al juego: Adivina el Número Secreto 🎯"
	Escribir "Tienes ", maxIntentos, " intentos para adivinar un número entre 1 y 100."

	Para intento <- 1 Hasta maxIntentos Con Paso 1
		Escribir ""
		Escribir "Intento ", intento, ": Ingresa tu número:"
		Leer numeroUsuario

		Si numeroUsuario = numeroSecreto Entonces
			gano <- Verdadero
			Salir
		SiNo
			Si numeroUsuario < numeroSecreto Entonces
				Escribir "🔼 El número secreto es MÁS ALTO."
			Sino
				Escribir "🔽 El número secreto es MÁS BAJO."
			FinSi
		FinSi
	FinPara

	Escribir ""
	Si gano Entonces
		Escribir "🎉 ¡Felicitaciones! Adivinaste el número en ", intento, " intentos."
	Sino
		Escribir "❌ Se te acabaron los intentos. El número secreto era: ", numeroSecreto
	FinSi

FinProceso
