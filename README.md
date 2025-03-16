Reloj Digital con Tkinter

Este proyecto es una aplicación de reloj digital simple creada con Python y la biblioteca Tkinter. Muestra la hora actual en un formato de 12 horas con AM/PM y se actualiza cada segundo.

📌 Requisitos

Para ejecutar este programa, necesitas tener instalado Python 3 en tu sistema. Tkinter viene incluido con Python por defecto, por lo que no es necesario instalar dependencias adicionales.

🚀 Ejecución

Para ejecutar el programa, simplemente corre el siguiente comando en tu terminal o línea de comandos:

python reloj.py

Asegúrate de que el archivo tenga el nombre correcto o ajusta el comando según corresponda.

📜 Explicación del Código

1. Importación de módulos

from tkinter import *
from tkinter.ttk import *
from time import strftime

tkinter se usa para crear la interfaz gráfica.

strftime de la biblioteca time se usa para obtener la hora actual en el formato deseado.

2. Creación de la ventana principal

root = Tk()
root.title('Reloj - Tarea 8 - 1910139')

Se inicializa una ventana con Tk().

Se establece el título de la ventana.

3. Función para actualizar la hora

def hora():
    datos = strftime('%I:%M:%S %p')
    label.config(text = datos)
    label.after(1000, hora)

strftime('%I:%M:%S %p') obtiene la hora en formato de 12 horas con AM/PM.

label.config(text = datos) actualiza el contenido del label con la nueva hora.

label.after(1000, hora) hace que la función se ejecute nuevamente después de 1 segundo.

4. Creación y configuración del Label

label = Label(root, font=('Old English Text MT', 60), padding='100', background='black', foreground='yellow')
label.pack(expand=True)

Se crea un Label que mostrará la hora con:

Fuente personalizada (Old English Text MT, tamaño 60).

Fondo negro y texto amarillo.

Relleno para mejorar la presentación.

pack(expand=True) para centrarlo en la ventana.

5. Llamada a la función y ejecución del programa

hora()
mainloop()

hora() inicia la actualización del reloj.

mainloop() mantiene la ventana abierta y en ejecución.

🖼️ Vista previa

Cuando ejecutas el programa, verás una ventana con un reloj digital estilizado que se actualiza cada segundo.

📌 Posibles Mejoras

Agregar fecha junto con la hora.

Permitir cambiar entre formato de 12h y 24h.

Agregar opciones de personalización de fuente y colores.

¡Disfruta programando tu reloj digital! ⏰
