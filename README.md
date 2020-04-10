# Edgar
Asistente Personal
print("ASISTENTE PERSONAL")
import unicodedata
nombre = input("\n¡Lo saludo con alegría! Por favor, deme su nombre: ")
print("\n¡Bienvenido seas, " + nombre + ".")
edad = float(input("¿Qué edad tienes? ")) 
if edad >= 18:
    print("\n¡Excelente! Un amigo para conversar! \n")
    preg = input("¿Vienes a sumar? ")
    while True:
        if unicodedata.normalize('NFKD', preg).encode('ASCII', 'ignore').strip().lower().upper() == unicodedata.normalize('NFKD', "Si").encode('ASCII', 'ignore').strip().lower().upper():
            print("\n¡Excelente! Comencemos. \n")
            num1 = float(input("Dame un número, cual sea: "))
            num2 = float(input("Dame otro número: "))
            resultado1 = num1 + num2
            print("\nSabemos que para todo número real existe una suma.")
            print("Tu suma es:", num1, "+", num2, "=", round(resultado1,2))
            print("\nEspero haberte ayudado.")
            break
        elif unicodedata.normalize('NFKD', preg).encode('ASCII', 'ignore').strip().lower().upper() == unicodedata.normalize('NFKD', "No").encode('ASCII', 'ignore').strip().lower().upper():
            print("\nEntonces, me despido.")
            break
        else:
            preg = input("\n¿Disculpa? ")

else:
    print("\nEres demasiado joven. Lo siento.")
