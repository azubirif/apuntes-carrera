---
title: Python
---
# Programación Orientada a Objetos (POO)
Permite programar realizando abstracciones. Consiste en definir plantillas que desarrollan como cada **objeto** (instancias de las clases) definirá sus atributos y los diferentes métodos que estos tienen:
- Clase
	- Atributos
	- Métodos

**Ejemplo**:
```
class Perro:
	# Atributos
	raza = ""
	edad = 0

	# Métoods
	def ladrar():
		...

	def comer():
		...
```

## Encapsulamiento
Es el concepto de aislar el funcionamiento de los métodos y variables de una clase.
# Declaración de clases
Para crear una clase, escribimos la palabra `class` seguido del nombre de la clase:
```
class Clase:
	pass

objeto = Clase()
```

Cada clase tiene atributos predefinido, pero luego tenemos los atributos de **instancia**, que permite al usuario modificar los atributos en su creación:
```
class Clase:
	def __init__(self, at1, at2):
		self.var1 = at1
		self.var2 = at2

obj = Clase(1, 2)
obj.var1 #1
obj.var2 #2
```

Las diferencias entre ambos es que los atributos de clase se almacenan en los *metadatos* de la clase, mientras que los de instancia se guardan en los *metadatos* del objeto.