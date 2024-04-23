# Reto-09---Brayux
PUNTO 1: Función Lambda
1.1) Calculo promedio de 5 números
```python
# Programa, calculo de promedio
if __name__=="__main__":
 # Declaramos las 5 variables
 a : float = float(input("Piense en un numero y digitelo: \n "))
 b : float = float(input("Digite un numero completo y seguido del dia, mes y año de su nacimiento\nejemplo, dia 19 mes 10 año 2005, numero resultante 19102005: \n "))
 c : float = float(input("Digite su edad sumando el año en el que estamos: \n "))
 d : float = float(input("Digite un numero re random: \n "))
 e : float = float(input("Preguntele a su amigo un numero mayor a 500 y escribalo: \n "))
 #Utilizamos la función Lambda
promedio = (lambda a,b,c,d,e:(a+b+c+d+e)/5)(a,b,c,d,e)
# Mostrar resultado funcion Anonima
print("El promedio de los números digitados es: ",promedio)
```
1.2) Peso de animales
```python
'''cantidad de carne de aves en kilos si se tienen N gallinas,
M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente.
'''
if __name__ == "__main__":
# nombramos las variables
 n: float= float(int(input("Cantidad de gallinas: ")))
 m: float= float(int(input("Cantidad de gallos: ")))
 k: float= float(int(input("Cantidad de pollitos: ")))
 #Utilizamos función lambda
 #Suponemos que una gallina pesa 6kg, un gallo 7kg y un pollito 1kg
masa=(lambda n,m,k:(n*6)+(m*7)+(k*1))(n,m,k)
print("El peso de ",n, "gallinas, ",m, "gallos y ",k, "pollitos es de ",masa, "kilos")

```
1.3) Función racional
```python
#Calcular una función Racional
if __name__ == "__main__":
 #Nombramos las variables
 z = float(input("Digite un número: "))
 #Utilizamos la función lambda
 fx= (lambda z : z/(z**(1/3)-1))(z)
 #Mostrar resultado
 print("El resultado de su funcion F(x) es: ",fx)
```
PUNTO 2: (*args).
2.1) Cuadrado de un número n
```python
def listado(*args)-> int: # Definimos variable
  cuadrado : int = 0 # inicializamos el programa
  for num in args: # para los numeros que hay en args aplicar el cuadrado
    cuadrado=num**2
  return cuadrado
if __name__ == "__main__": 
    a = int(input("Ingrese numero : ")) 
    print("el cuadrado del numero es " + str(listado(a)))

```
2.2) Factorial Número
```python
def factorial(*args)-> int: # Definimos variable
   for num in args: # para los numeros que hay en args aplicar la condicion impuesta
       a = 1
       b = 1
       while a <= num:# se hace un bucle para poder realizar el factorial del numero
        b = b * a
        a += 1
   return b
if __name__ == "__main__":
    c = int(input("Ingrese numero : "))
    if 0 <= c:
       print("el factorial del numero es " + str(factorial(c)))
    else:
     print("Digtaste un número fuera de los parametros")

```
2.3) ASCCI
```python
def ASCII(*args)-> int: #definimos l variable
     for num in args: #para los numeros que hay en args aplicar la condicion impuesta en a,la cual es convertir un entero a codigo ASCII
      a=(chr(num))
     return a
if __name__ == "__main__":
      a = int(input("Digite un numero entero"))
      if a > 97 and a < 122: #establecemos un intervalo donde tiene sentido el código ASCII
        print("El numero entero corresponde a una vocal minuscula en el codigo ASCII, es:"+(ASCII(a)))
      else:
        print("No corresponde a una vocal minuscula en el codigo ASCII")

```

PUNTO 3: Función recursiva para calcular la operación de la potencia.
```python
'''función recursiva para la potencia de un número
creamos una función'''
def potencia(num1,num2):
    '''Ordenamos al programa restricciones para seguir operando
    si el exponente es 0 o 1 el resultado es inmediato,
    sin embargo si es diferente de estos, se le debera restar 1'''
    if num2 ==0:
        return 1
    elif num1 == 0:
        return 0
    elif num2==1:
        return num1
    else:
        return num1 * potencia(num1, num2-1)
   
if __name__=="__main__":
    num1=float(input("Digite numero 1: "))
    num2=float(input("Digite numero 2: "))
    print("Su numero es: "+str(potencia(num1,num2)))

```

PUNTO 4: Utilice la siguiente plantilla de code para contar el tiempo:
```python
import time
start_time = time.time()
# instrucciones sobre las cuales se quiere medir tiempo de ejecución
end_time = time.time()

timer = end_time - start_time
print(timer)
```
////// fibonacci con iteración o con recursión ///////
[![Whats-App-Image-2024-04-22-at-8-41-21-PM.jpg](https://i.postimg.cc/RhnKgMnF/Whats-App-Image-2024-04-22-at-8-41-21-PM.jpg)](https://postimg.cc/1Vs8t1Bh)
```python
import time
def funcion_recursiva_fibonacci(Número = "")->float:
    if Número <= 1:
        return Número
    else:
        return funcion_recursiva_fibonacci(Número - 1) + funcion_recursiva_fibonacci(Número - 2)
def fibonacci_tiempo()->float:
    bandera_10 = False
    Número = 1
    while True:
        start_time = time.time()
        funcion_recursiva_fibonacci(Número)
        end_time = time.time()
        timer = end_time - start_time
        Número += 1
        print(f"El tiempo entre el número {Número - 1} y el {Número} de la serie de Fibonacci es: {timer} ")
        # Si tarda más de 5 segundos la bandera se activa y se detiene el bucle while
        if timer >= 5 and bandera_10 == False:
            bandera_10 = True
            break
if __name__ == "__main__":
    print("inicio el programa")
    fibonacci_tiempo()
```
PUNTO 5: Cuenta stackoverflow
[![Whats-App-Image-2024-04-11-at-8-15-20-PM.jpg](https://i.postimg.cc/Xv0HFzmd/Whats-App-Image-2024-04-11-at-8-15-20-PM.jpg)](https://postimg.cc/k2fvPfng)
PUNTO 6: Cuenta Linkedin
[![Whats-App-Image-2024-04-22-at-8-38-23-PM.jpg](https://i.postimg.cc/QdZknWmr/Whats-App-Image-2024-04-22-at-8-38-23-PM.jpg)](https://postimg.cc/RNGHWh2P)
esta en proceso de verificación porq creen q soy un botcito :(

