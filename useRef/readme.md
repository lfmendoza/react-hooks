# Cronómetro con React Hooks

## Descripción

Este proyecto implementa un cronómetro utilizando React Hooks para gestionar el estado y la lógica del componente. El cronómetro permite iniciar, pausar, reiniciar y guardar sesiones de tiempo, mostrando una lista de las sesiones guardadas.

## Características

- Visualización del tiempo en formato mm:ss:ms
- Control de inicio/pausa con un solo botón
- Función de reinicio que pone el contador a cero
- Guardado de sesiones con su respectivo tiempo
- Visualización de una lista de sesiones guardadas

## Tecnologías utilizadas

- React 18
- Hooks (useState, useEffect, useRef)
- Tailwind CSS para estilos
- Babel para compilar JSX

## Implementación

El componente principal Stopwatch utiliza:

- `useState` para manejar:
  - El tiempo actual (time)
  - El estado de ejecución (isRunning)
  - La lista de sesiones guardadas (sessions)
- `useEffect` para:
  - Iniciar el temporizador cuando isRunning es true
  - Detener el temporizador cuando isRunning es false
  - Limpiar el intervalo cuando el componente se desmonta
- `useRef` para:
  - Guardar el ID del intervalo sin causar re-renders
  - Mantener el tiempo acumulado entre pausas
  - Guardar el tiempo de inicio para calcular el tiempo transcurrido

## Hooks utilizados

1. **useState**:

   - Maneja el estado del tiempo, el estado de ejecución y la lista de sesiones
   - Permite actualizar la interfaz cuando estos valores cambian

2. **useEffect**:

   - Controla el ciclo de vida del temporizador
   - Se ejecuta cuando el estado de ejecución cambia
   - Incluye una función de limpieza para evitar memory leaks

3. **useRef**:
   - Almacena el ID del intervalo
   - Guarda referencias a valores que no deben causar re-renders
   - Mantiene valores entre renders sin afectar al ciclo de renderizado

## Instalación y uso

1. Clona este repositorio
2. Abre el archivo `index.html` en tu navegador

## Demo en vivo

Proyecto funcionando en: [http://awita.site/usuarios/men19644/react-hooks/useRef](http://awita.site/usuarios/men19644/react-hooks/useRef)

## Estructura del proyecto

```
.
├── index.html     # Archivo HTML con CDN de React y código JSX
└── README.md      # Este archivo
```

## Autor

Fernando Mendoza

## Licencia

MIT
