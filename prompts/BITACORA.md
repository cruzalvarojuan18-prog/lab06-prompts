# Bitacora de prompts
Laboratorio 06: Fundamentos de Ingenieria de Prompts
Herramienta de IA usada: ChatGPT / Gemini

## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|---|---|---|
| Los estudiantes programan en Java. | 35 | 7 |
| The students program in Java. | 29 | 6 |
| desafortunadamente | 18 | 4 |

**Observaciones de la Ventana de Contexto:**
Al preguntar por TiendaTec dentro del mismo chat, la IA respondió correctamente porque los datos estaban dentro de su ventana de contexto. Al abrir un chat nuevo y hacer la misma pregunta, la IA no supo responder debido a que la ventana de contexto se reinicia estando vacía.

## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|---|---|---|
| 0 | 100.0% | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 | 68.3% | BiblioTec, LibroYa, BiblioTec, BiblioTec, PrestaLibro |
| 1.0 | 44.2% | BiblioTec, LibroYa, LectoGo, BiblioTec, PrestaLibro |
| 1.8 | 32.1% | LectoGo, BiblioTec, NubeDeTinta, LibroYa, PaginaLibre |

**Observación:** Al aumentar la temperatura la variedad de nombres aumenta porque las probabilidades se reparten. El simulador nunca inventa nombres nuevos porque la temperatura solo afecta cómo selecciona opciones existentes en su lista.

## Ejercicio 4: Prompt vago vs estructurado

| Criterio | Prompt vago | Prompt estructurado |
|---|---|---|
| Menciona el objetivo del sistema | No | Sí |
| Menciona a los usuarios principales | No | Sí |
| Tiene exactamente 3 funcionalidades | No | Sí |
| Esta en 3 parrafos | No | Sí |
| Lo usaria en un informe real | No | Sí |

## Ejercicio 5: Anatomia de un prompt

| Componente | Texto de mi prompt |
|---|---|
| Rol | Actua como desarrollador Java |
| Instruccion | Crea un programa en Java |
| Contexto | Para gestionar los productos de una tienda, usando una clase Producto con los atributos codigo, nombre, precio y stock |
| Ejemplo | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio) |
| Formato | Explica primero la estructura de la clase y luego presenta el codigo Java |

## Ejercicio 6: Del prompt basico al profesional

Prompt Profesional:
Actua como desarrollador Java. Crea un ejemplo de login para una aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases.

Mejora (Iteración):
Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.