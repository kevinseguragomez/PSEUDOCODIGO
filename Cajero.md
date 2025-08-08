Proceso CajeroAutomatico
	
	// Declaración de variables
	Definir saldo, retiro Como Real;
	
	// Inicialización del saldo disponible
	saldo <- 500;
	
	// Solicitar el monto a retirar al usuario
	Escribir "Bienvenido al cajero automático.";
	Escribir "Su saldo actual es: ", saldo, " pesos.";
	Escribir "";
	Escribir "¿Cuánto dinero desea retirar?";
	Leer retiro;
	
	// Verificar si el monto a retirar es válido y si hay saldo suficiente
	Si (retiro > 0) y (retiro <= saldo) Entonces
		// Si el saldo es suficiente, se realiza el retiro
		saldo <- saldo - retiro;
		Escribir "Retire su dinero. El monto retirado es de: ", retiro, " pesos.";
		Escribir "Su nuevo saldo es: ", saldo, " pesos.";
	SiNo
		// Si el saldo es insuficiente o el monto no es válido
		Si (retiro <= 0) Entonces
			Escribir "El monto ingresado no es válido. Por favor, ingrese un valor positivo.";
		SiNo
			Escribir "Fondos insuficientes. Su saldo actual es de: ", saldo, " pesos.";
		FinSi
	FinSi
	
FinProceso