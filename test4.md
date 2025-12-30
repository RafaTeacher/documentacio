# Lección de Tkinter para Principiantes
## Ejemplos Progresivos para Estudiantes de 16 años

---

## Ejemplo 1: Tu Primera Ventana

### Objetivo
Crear una ventana básica vacía para entender la estructura mínima de una aplicación Tkinter.

### Código
```python
import tkinter as tk

# Crear la ventana principal
ventana = tk.Tk()

# Configurar el título de la ventana
ventana.title("Mi Primera Ventana")

# Configurar el tamaño de la ventana
ventana.geometry("400x300")

# Mantener la ventana abierta
ventana.mainloop()
```

### Explicación
1. **`import tkinter as tk`**: Importamos la librería Tkinter con el alias `tk` para escribir menos.
2. **`tk.Tk()`**: Crea la ventana principal de nuestra aplicación.
3. **`.title()`**: Establece el texto que aparece en la barra de título.
4. **`.geometry()`**: Define el tamaño de la ventana (ancho x alto en píxeles).
5. **`.mainloop()`**: Mantiene la ventana abierta y responde a las interacciones del usuario.

### ¡Pruébalo!
Ejecuta este código y verás una ventana vacía de 400x300 píxeles con el título "Mi Primera Ventana".

---

## Ejemplo 2: Añadiendo tu Primer Texto

### Objetivo
Agregar un elemento visual (etiqueta con texto) a nuestra ventana.

### Código
```python
import tkinter as tk

# Crear la ventana principal
ventana = tk.Tk()
ventana.title("Ventana con Texto")
ventana.geometry("400x300")

# Crear una etiqueta con texto
etiqueta = tk.Label(ventana, text="¡Hola, mundo!")

# Mostrar la etiqueta en la ventana
etiqueta.pack()

# Mantener la ventana abierta
ventana.mainloop()
```

### Explicación
**Nuevos conceptos:**
1. **`tk.Label()`**: Crea una etiqueta que puede mostrar texto o imágenes.
   - El primer parámetro (`ventana`) indica dónde colocar la etiqueta
   - `text=` especifica qué texto mostrar
2. **`.pack()`**: Coloca automáticamente el elemento en la ventana de forma ordenada.

### ¡Pruébalo!
Ahora verás el texto "¡Hola, mundo!" centrado en tu ventana.

---

## Ejemplo 3: Personalizando el Texto

### Objetivo
Aprender a cambiar la apariencia del texto (fuente, tamaño, color).

### Código
```python
import tkinter as tk

# Crear la ventana principal
ventana = tk.Tk()
ventana.title("Texto Personalizado")
ventana.geometry("400x300")

# Crear una etiqueta con texto personalizado
etiqueta = tk.Label(
    ventana, 
    text="¡Python es genial!",
    font=("Arial", 20),
    fg="blue",
    bg="yellow"
)

# Mostrar la etiqueta en la ventana
etiqueta.pack()

ventana.mainloop()
```

### Explicación
**Nuevos parámetros de `Label`:**
1. **`font=("Arial", 20)`**: Define la fuente y el tamaño del texto.
   - Primer valor: nombre de la fuente
   - Segundo valor: tamaño en puntos
2. **`fg="blue"`**: Color del texto (foreground = primer plano).
3. **`bg="yellow"`**: Color de fondo de la etiqueta (background = fondo).

### Colores disponibles
Puedes usar nombres en inglés como: "red", "green", "blue", "purple", "orange", "black", "white", etc.

### ¡Pruébalo!
Experimenta cambiando los colores y el tamaño de la fuente.

---

## Ejemplo 4: Tu Primer Botón

### Objetivo
Crear un botón que el usuario pueda hacer clic (aunque aún no haga nada).

### Código
```python
import tkinter as tk

# Crear la ventana principal
ventana = tk.Tk()
ventana.title("Mi Primer Botón")
ventana.geometry("400x300")

# Crear una etiqueta
etiqueta = tk.Label(
    ventana, 
    text="¡Haz clic en el botón!",
    font=("Arial", 16)
)
etiqueta.pack()

# Crear un botón
boton = tk.Button(
    ventana,
    text="¡Clic aquí!",
    font=("Arial", 12),
    bg="lightblue"
)
boton.pack()

ventana.mainloop()
```

### Explicación
**Nuevo elemento:**
1. **`tk.Button()`**: Crea un botón clickeable.
   - Usa parámetros similares a `Label`: `text`, `font`, `bg`, etc.
   - Los botones por defecto tienen un borde y cambian de apariencia al hacer clic.

**Observación:** El botón se puede hacer clic, pero aún no hace nada útil. ¡Eso lo veremos en el siguiente ejemplo!

### ¡Pruébalo!
Haz clic en el botón y observa cómo cambia visualmente cuando lo presionas.

---

## Ejemplo 5: Botón que Hace Algo

### Objetivo
Crear un botón que ejecute una acción cuando se hace clic en él.

### Código
```python
import tkinter as tk

# Crear la ventana principal
ventana = tk.Tk()
ventana.title("Botón Interactivo")
ventana.geometry("400x300")

# Función que se ejecuta al hacer clic
def saludar():
    etiqueta.config(text="¡Hola! Hiciste clic en el botón")

# Crear una etiqueta
etiqueta = tk.Label(
    ventana, 
    text="Haz clic en el botón para saludar",
    font=("Arial", 14)
)
etiqueta.pack(pady=10)

# Crear un botón que ejecute la función saludar
boton = tk.Button(
    ventana,
    text="Saludar",
    font=("Arial", 12),
    bg="lightgreen",
    command=saludar
)
boton.pack(pady=10)

ventana.mainloop()
```

### Explicación
**Nuevos conceptos:**
1. **Función `saludar()`**: Define qué hacer cuando se hace clic en el botón.
2. **`.config(text="...")`**: Cambia el texto de la etiqueta después de crearla.
3. **`command=saludar`**: Conecta el botón con la función (¡sin paréntesis!).
4. **`pady=10`**: Añade espacio vertical alrededor del elemento.

**¡Importante!** 
- Escribimos `command=saludar` (sin paréntesis)
- No `command=saludar()` (con paréntesis)

### ¡Pruébalo!
Haz clic en el botón y observa cómo cambia el texto de la etiqueta.

---

## Resumen de lo Aprendido

En estos 5 ejemplos has aprendido:
1. ✅ Crear ventanas básicas
2. ✅ Añadir texto con `Label`
3. ✅ Personalizar colores y fuentes
4. ✅ Crear botones con `Button`
5. ✅ Hacer que los botones ejecuten funciones
6. ✅ Usar `.pack()` para organizar elementos
7. ✅ Modificar elementos con `.config()`

## Ejercicio de Práctica
Crea una ventana que tenga:
- Un título personalizado
- Una etiqueta con tu nombre
- Un botón que cambie el color de fondo de la etiqueta cuando hagas clic
