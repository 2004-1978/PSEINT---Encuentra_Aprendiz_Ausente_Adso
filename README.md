Algoritmo Encuentra_Aprendiz_Ausente_Adso
		Definir aprendices, presentes, ausentes Como Caracter
		Definir nombre, aprendiz, presente, ausente Como Caracter
		Definir totalPresentes, contador, contadorAusentes Como Entero
		Definir encontrado Como Logico
		
		Dimension aprendices[27]
		Dimension presentes[27]
		Dimension ausentes[27]
		
		// Ingresar los nombres de los 27 aprendices
		Para contador <- 1 Hasta 27 Hacer
			Escribir "Ingrese el nombre del aprendiz ", contador, ":"
			Leer nombre
			aprendices[contador] <- nombre
		FinPara
		
		// Leer cuántos asistieron
		Escribir "Ingrese la cantidad de aprendices que asistieron hoy:"
		Leer totalPresentes
		
		Para contador <- 1 Hasta totalPresentes Hacer
			Escribir "Ingrese el nombre del aprendiz presente:"
			Leer nombre
			presentes[contador] <- nombre
		FinPara
		
		// Buscar ausentes
		contadorAusentes <- 1
		Para contador <- 1 Hasta 27 Hacer
			aprendiz <- aprendices[contador]
			encontrado <- Falso
			
			Para contador2 <- 1 Hasta totalPresentes Hacer
				presente <- presentes[contador2]
				Si aprendiz = presente Entonces
					encontrado <- Verdadero
				FinSi
			FinPara
			
			Si No encontrado Entonces
				ausentes[contadorAusentes] <- aprendiz
				contadorAusentes <- contadorAusentes + 1
			FinSi
		FinPara
		
		// Mostrar ausentes
		Escribir "Los aprendices ausentes hoy son:"
		Para contador <- 1 Hasta contadorAusentes - 1 Hacer
			Escribir "- ", ausentes[contador]
		FinPara
FinAlgoritmo
