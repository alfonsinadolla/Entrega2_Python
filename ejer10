#10. Dada una lista de nombres de estudiantes y dos listas con sus notas en un curso, escriba un
#programa que manipule dichas estructuras de datos para poder resolver los siguientes puntos:
#A. Generar una estructura con todas las notas relacionando el nombre del estudiante con las
#notas. Utilizar esta estructura para la resolución de los siguientes items.
#B. Calcular el promedio de notas de cada estudiante.
#C. Calcular el promedio general del curso.
#D. Identificar al estudiante con la nota promedio más alta.
#E. Identificar al estudiante con la nota más baja.

nombres = ''' 'Agustin', 'Alan', 'Andrés', 'Ariadna', 'Bautista', 'CAROLINA', 'CESAR',
'David','Diego', 'Dolores', 'DYLAN', 'ELIANA', 'Emanuel', 'Fabián', 'Facundo',
'Francsica', 'FEDERICO', 'Fernanda', 'GONZALO', 'Gregorio', 'Ignacio', 'Jonathan',
'Joaquina', 'Jorge','JOSE', 'Javier', 'Joaquín' , 'Julian', 'Julieta', 'Luciana',
'LAUTARO', 'Leonel', 'Luisa', 'Luis', 'Marcos', 'María', 'MATEO', 'Matias',
'Nicolás', 'Nancy', 'Noelia', 'Pablo', 'Priscila', 'Sabrina', 'Tomás', 'Ulises',
'Yanina' '''

notas_1 = [81, 60, 72, 24, 15, 91, 12, 70, 29, 42, 16, 3, 35, 67, 10, 57, 11, 69,
12, 77, 13, 86, 48, 65, 51, 41, 87, 43, 10, 87, 91, 15, 44,
85, 73, 37, 42, 95, 18, 7, 74, 60, 9, 65, 93, 63, 74]

notas_2 = [30, 95, 28, 84, 84, 43, 66, 51, 4, 11, 58, 10, 13, 34, 96, 71, 86, 37,
64, 13, 8, 87, 14, 14, 49, 27, 55, 69, 77, 59, 57, 40, 96, 24, 30, 73,
95, 19, 47, 15, 31, 39, 15, 74, 33, 57, 10]

def generar_estructura(nombres,notas_1,notas_2):
    nombres = [nombre.strip().strip("'") for nombre in nombres.split(',')]
    notas = list(zip(notas_1, notas_2))
    diccionario_notas = dict(zip(nombres, notas))
    return diccionario_notas

def calcular_promedios(diccionario_notas):
    promedios = dict(map(lambda x: (x[0], sum(x[1])/2), zip(diccionario_notas.keys(), diccionario_notas.values())))
    return promedios

def calcular_promedio_general(diccionario_notas):
    notas = list(zip(*diccionario_notas.values()))
    promedio_general = sum(map(lambda x: sum(x), notas)) / len(notas[0]) / len(notas)
    return promedio_general

def calcular_promedio_mas_alto(promedios,nombres):
    max_promedio = max(promedios.values())
    estudiante = next((estudiante for estudiante, promedio in promedios.items() if promedio == max_promedio), None)
    return max_promedio,estudiante

def identificar_estudiante_nota_mas_baja(promedios):
    estudiante_nota_mas_baja = min(promedios, key=promedios.get)
    return estudiante_nota_mas_baja

if __name__ == "__main__":
    print("-" * 100)
    diccionario_notas= generar_estructura(nombres,notas_1,notas_2)
    print(diccionario_notas)

    promedios=calcular_promedios(diccionario_notas)
    print(f"\nPromedio de todos los alumnos: {promedios}")

    promedio_general=calcular_promedio_general(diccionario_notas)
    print(f"\nPromedio general: {promedio_general}")

    promedio, estudiante = calcular_promedio_mas_alto(promedios, nombres)
    print(f"El estudiante con el promedio más alto es {estudiante}, con {promedio}") 

    estudiante_nota_mas_baja = identificar_estudiante_nota_mas_baja(promedios)
    print("El estudiante con la nota más baja es:", estudiante_nota_mas_baja)   
    print("-" * 100)