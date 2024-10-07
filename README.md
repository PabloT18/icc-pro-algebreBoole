## Algebra Boole - Python 

Aplicar las leyes de algrebra de Boole para resolver los siguientes ejercicios.


### **Ejercicio 1: Simplificación de una Condición Compleja**

#### **Enunciado:**

Tienes el siguiente código en Python, que representa una condición lógica para activar una alarma de seguridad. La condición es demasiado larga y necesita ser optimizada:

```python
def activar_alarma(A, B, C):
    if (A and B) or (A and not B) or (not A and C):
        return "Alarma activada"
    else:
        return "Alarma desactivada"
```

**Pregunta**: ¿Cómo podrías simplificar la condición en la función para que sea más eficiente? Aplica las leyes del álgebra de Boole para reducir la expresión lógica.

---

### **Ejercicio 2: Reducción de Condición en un Sistema de Control**

#### **Enunciado:**

Un sistema de control en una fábrica determina si debe encender una máquina de seguridad dependiendo de varios sensores:

```python
if (A and B) or (A and not C) or (not A and B) or (not A and not B):
    print ("Encender Máquina")
else:
     print ("Apagar Máquina")
```

**Pregunta**: Simplifica la condición lógica utilizando las leyes del álgebra de Boole para hacer el código más legible y eficiente.

---

### **Ejercicio 3: Verificación de Acceso**
#### **Enunciado:**
Una aplicación web utiliza una lógica compleja para verificar si un usuario tiene acceso a ciertos recursos. El código actual es el siguiente:

```python
admin= True
usuario_activo= True
tiene_permiso = False
if (admin and usuario_activo) or (admin and not tiene_permiso) or (not admin and usuario_activo):
    return "Acceso Permitido"
else:
    return "Acceso Denegado"
```

**Pregunta**: ¿Cómo puedes simplificar la condición lógica para optimizar el código? Aplica las leyes del álgebra de Boole para reducir la cantidad de evaluaciones necesarias.

---

### **Ejercicio 4: Detección de Movimiento**

#### **Enunciado:**

Un sistema de detección de movimiento utiliza sensores que generan un patrón de activación para encender las luces automáticamente. El código para encender las luces es el siguiente:

```python
sensor1 =  True
sensor2 = False
sensor3 = False
if (sensor1 and sensor2) or (sensor1 and not sensor2) or (not sensor1 and sensor3):
    print ( "Luces encendidas")
else:
    print ( "Luces apagadas")
```

**Pregunta**: Aplica las leyes del álgebra de Boole para simplificar esta expresión y mejorar la eficiencia del sistema.

---

### **Ejercicio 5: Sistema de Ventilación**

#### **Enunciado:**

El sistema de ventilación de un edificio se activa si las condiciones de temperatura y CO2 son críticas. El código original utiliza una condición lógica larga:

```python
temp_alta = True
co2_alto= True
puerta_abierta= True
if (temp_alta and co2_alto) or (temp_alta and not puerta_abierta) or (not temp_alta and co2_alto):
    print( "Ventilación Activada")
else:
    print( "Ventilación Desactivada")
```

**Pregunta**: Simplifica la condición utilizando las leyes del álgebra de Boole y optimiza el código.

---

### **Ejercicio 6: Sistema de Luces de Emergencia**

En un sistema de luces de emergencia, las luces se encienden si se cumplen ciertas condiciones. El código que lo controla es el siguiente:

```python
encendido_general = True
bateria_baja = True
fallo_sistema = True
if (encendido_general and bateria_baja) or (encendido_general and fallo_sistema) or (not encendido_general and bateria_baja):
    print( "Luces de emergencia activadas)
else:
    print( "Luces de emergencia desactivadas")
```

**Pregunta**: Utiliza las leyes del álgebra de Boole para simplificar esta condición lógica.

---

### **Ejercicio 7: Control de Entrada a un Edificio**

#### **Enunciado:**

Un edificio utiliza una serie de sensores para verificar si se debe permitir la entrada a un visitante. El sistema actual tiene la siguiente lógica:

```python
def permitir_entrada(huella, tarjeta, permiso_especial):
    if (huella and tarjeta) or (huella and not permiso_especial) or (not huella and permiso_especial):
        return "Entrada permitida"
    else:
        return "Entrada denegada"
```

**Pregunta**: ¿Puedes simplificar esta condición usando las leyes del álgebra de Boole?



### **Guía para resolver los ejercicios**

Para resolver estos ejercicios, los estudiantes deberán aplicar las siguientes leyes del álgebra de Boole:

1. **Ley de Identidad:**
   - \( A \cdot 1 = A \)
   - \( A + 0 = A \)

2. **Ley de Anulación:**
   - \( A \cdot 0 = 0 \)
   - \( A + 1 = 1 \)

3. **Ley de Idempotencia:**
   - \( A \cdot A = A \)
   - \( A + A = A \)

4. **Ley de Complemento:**
   - \( A \cdot \overline{A} = 0 \)
   - \( A + \overline{A} = 1 \)

5. **Ley Distributiva:**
   - \( A \cdot (B + C) = A \cdot B + A \cdot C \)
   - \( A + (B \cdot C) = (A + B) \cdot (A + C) \)

6. **Ley de Absorción:**
   - \( A + (A \cdot B) = A \)
   - \( A \cdot (A + B) = A \)

7. **Leyes de De Morgan:**
   - \( \overline{A \cdot B} = \overline{A} + \overline{B} \)
   - \( \overline{A + B} = \overline{A} \cdot \overline{B} \)

---

## **Soluciones esperadas:**

Al simplificar las condiciones largas en estos ejercicios, los estudiantes deben enfocarse en:

- **Eliminar redundancias:** Si una expresión tiene términos como \( A + A \) o \( A \cdot A \), pueden reducirse a \( A \).
- **Aplicar las leyes de complemento:** Si ven expresiones como \( A \cdot \overline{A} \) o \( A + \overline{A} \), deben reemplazarlas con 0 o 1, respectivamente.
- **Usar la ley de absorción:** Para eliminar términos que no afectan el resultado, como \( A + (A \cdot B) \) se simplifica a \( A \).

Por ejemplo, en el **Ejercicio 1**, la condición original:

```python
if (A and B) or (A and not B) or (not A and C):
```

**Se puede simplificar** aplicando la ley de complementos y absorción a:

```python
if A or (not A and C):
```

Y finalmente:

```python
if A or C:
```

---

## **Conclusión**

Estos ejercicios proporcionan una excelente oportunidad para que los estudiantes practiquen la **simplificación de expresiones booleanas** en un contexto de programación. Al entender cómo funcionan las leyes del álgebra de Boole, podrán optimizar el código, mejorando tanto su legibilidad como su eficiencia.

Al simplificar las condiciones lógicas en estos ejemplos, el código resultante será más fácil de mantener, más rápido de ejecutar y más claro para cualquier desarrollador que trabaje en el proyecto. ¡Espero que estos ejercicios sean útiles para practicar!


## Contribute

To contribute to this project, please create a fork and send a pull request, or simply open an issue with your comments and suggestions.

## Authors

- [PABLO TORRES] - Initial development