# Valdar_Operadores

def verificar_palabra():
    palabra = input("Ingresa una palabra: ").strip()
    longitud = len(palabra)

   if longitud == 0:          #condiciones para respuesta
        print("❌ No se ingresó ninguna palabra.\n")
    elif 4 <= longitud <= 8:
        print("✅ La palabra es correcta.\n")
    elif longitud < 4:
        print(f"❌ Hacen falta letras. Solo tiene {longitud} letras.\n")
    else:
        print(f"❌ Sobran letras. Tiene {longitud} letras.\n")


def verificar_cuadrante():
    try: #captura datos
        x = float(input("Ingrese la coordenada X: "))
        y = float(input("Ingrese la coordenada Y: "))
        if x == 0 or y == 0: #menú de condiciones para identificar cuadrante
            print("❌ Ninguna coordenada debe ser 0.\n")
        elif x > 0 and y > 0:
            print("✅ El punto se encuentra en el cuadrante I\n")
        elif x < 0 and y > 0:
            print("✅ El punto se encuentra en el cuadrante II\n")
        elif x < 0 and y < 0:
            print("✅ El punto se encuentra en el cuadrante III\n")
        elif x > 0 and y < 0:
            print("✅ El punto se encuentra en el cuadrante IV\n")
    except ValueError:  #corrobora datos ingresados
        print("❌ Debes ingresar valores numéricos válidos para las coordenadas.\n")


def mostrar_menu(): #menú principal
    print("=== MENÚ PRINCIPAL ===")
    print("Selecciona una opción")
    print("1. Verificar longitud de una palabra")
    print("2. Encontrar cuadrante de un punto")
    print("3. Salir")


def programa_principal(): #main
    while True: #condicionales del menú
        mostrar_menu()
        opcion = input("Selecciona una opción (1-3): ").strip()
        if opcion == "1":
            verificar_palabra()
        elif opcion == "2":
            verificar_cuadrante()
        elif opcion == "3":
            print("👋 Saliendo del programa. ¡Hasta luego!")
            break
        else:
            print("❌ Opción no válida. Intenta nuevamente.\n")


# Ejecutar el programa
programa_principal()
