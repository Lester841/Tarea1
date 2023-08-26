# PSeInt 
Algoritmo tarea1
    Definir cm, resultado Como Real
    Definir opcion Como Entero
	
    Escribir "Ingrese la longitud en centímetros:"
    Leer cm
	
    Escribir "Opciones de conversión:"
    Escribir "1. Metros"
    Escribir "2. Yardas"
    Escribir "3. Varas"
    Escribir "4. Pulgadas"
    Escribir "5. Pies pseint"
    Escribir "Seleccione la opción de conversión (1/2/3/4/5):"
    Leer opcion
	
    Segun opcion Hacer
        1:
            resultado = cm / 100
            Escribir cm, " centímetros son ", resultado, " metros."
        2:
            resultado = cm / 91.44
            Escribir cm, " centímetros son ", resultado, " yardas."
        3:
            resultado = cm / 84.39
            Escribir cm, " centímetros son ", resultado, " varas."
        4:
            resultado = cm / 2.54
            Escribir cm, " centímetros son ", resultado, " pulgadas."
        5:
            resultado = cm / 31.415
            Escribir cm, " centímetros son ", resultado, " pies ."
        De Otro Modo:
            Escribir "Opción no válida. Por favor, seleccione una opción válida."
    Fin Segun

FinAlgoritmo

## C++
#include <iostream>
#include <string>

double centimeters_to_other_units(double value_cm, std::string target_unit) {
    if (target_unit == "metros") {
        return value_cm / 100.0;
    } else if (target_unit == "yardas") {
        return value_cm / 91.44;
    } else if (target_unit == "varas") {
        return value_cm / 84.39;
    } else if (target_unit == "pulgadas") {
        return value_cm / 2.54;
    } else if (target_unit == "pies") {
        return value_cm / 30.48;
    } else {
        return -1.0; // Valor inválido para indicar error
    }
}

int main() {
    try {
        double cm_value;
        std::string target_unit;

        std::cout << "Ingrese la longitud en centímetros: ";
        std::cin >> cm_value;

        std::cout << "Ingrese la unidad a la que desea convertir (metros/yardas/varas/pulgadas/pies): ";
        std::cin >> target_unit;

        double converted_value = centimeters_to_other_units(cm_value, target_unit);

        if (converted_value != -1.0) {
            std::cout << cm_value << " centímetros equivalen a " << converted_value << " " << target_unit << "." << std::endl;
        } else {
            std::cout << "Unidad de conversión no válida. Por favor, elija entre metros, yardas, varas, pulgadas o pies." << std::endl;
        }

    } catch (...) {
        std::cout << "Error . Asegúrese de ingresar un número válido ." << std::endl;
    }

    return 0;
}  
### Python 
def centimeters_to_meters(cm):
    return cm / 100

def centimeters_to_yards(cm):
    return cm / 91.44

def centimeters_to_varas(cm):
    return cm / 84.39

def centimeters_to_inches(cm):
    return cm / 2.54

def centimeters_to_feet_in_peseint(cm):
    return cm / 31.415

def main():
    try:
        cm = float(input("Ingrese la longitud en centímetros: "))
        print("Opciones de conversión:")
        print("1. Metros")
        print("2. Yardas")
        print("3. Varas")
        print("4. Pulgadas")
        print("5. Pies en peseint")
        option = int(input("Seleccione la opción de conversión (1/2/3/4/5): "))
        
        if option == 1:
            result = centimeters_to_meters(cm)
            print(f"{cm} centímetros son {result} metros.")
        elif option == 2:
            result = centimeters_to_yards(cm)
            print(f"{cm} centímetros son {result} yardas.")
        elif option == 3:
            result = centimeters_to_varas(cm)
            print(f"{cm} centímetros son {result} varas.")
        elif option == 4:
            result = centimeters_to_inches(cm)
            print(f"{cm} centímetros son {result} pulgadas.")
        elif option == 5:
            result = centimeters_to_feet_in_peseint(cm)
            print(f"{cm} centímetros son {result} pies en peseint.")
        else:
            print("Opción no válida. Por favor, seleccione una opción válida.")

    except ValueError:
        print("Por favor, ingrese un número válido.")

if __name__ == "__main__":
    main()

