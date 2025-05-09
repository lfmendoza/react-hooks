# Renderizado de Hijos con useCallback

## Descripción

Este proyecto demuestra cómo el uso de `useCallback` puede prevenir re-renderizados innecesarios en componentes hijos. Ilustra cómo las funciones creadas en cada renderizado causan que los componentes hijos se vuelvan a renderizar incluso cuando utilizamos `memo`.

## Objetivos de Aprendizaje

- Entender por qué las funciones nuevas en cada render causan re-renders innecesarios
- Aprender a usar useCallback para memorizar funciones
- Comprender cómo pasar funciones a componentes hijos manteniendo la optimización

## Componentes Implementados

### 1. Card (Componente Principal)

- Utiliza `useState` para gestionar:
  - `randomNumber`: Almacena el número aleatorio generado
  - `counter`: Contador que se incrementa con el botón normal
- Implementa dos funciones:
  - `createRandom`: Genera un número aleatorio (optimizada con useCallback)
  - `addCounter`: Incrementa el contador (sin optimizar)

### 2. ButtonOptimizado

- Componente de botón optimizado con `memo`
- Solo se renderiza cuando sus props cambian
- Recibe una función vía props

### 3. ButtonNormal

- Componente de botón regular (sin optimización)
- Se renderiza en cada render del componente padre
- Recibe una función vía props

## Conceptos Demostrados

### useCallback

- Memoriza una función entre renderizados
- Evita que se cree una nueva referencia de función en cada render
- Mejora el rendimiento al evitar re-renders innecesarios

### memo

- Memoriza el resultado del renderizado de un componente
- Previene re-renders cuando las props no cambian
- Solo funciona correctamente con `useCallback` cuando se pasan funciones

## Flujo de Demostración

1. Al hacer clic en "Incrementar Contador":
   - La función `addCounter` se crea nuevamente en cada render
   - Ambos botones se vuelven a renderizar (incluso el optimizado)
2. Al hacer clic en "Generar Aleatorio":
   - La función `createRandom` mantiene la misma referencia gracias a useCallback
   - Solo se renderiza de nuevo el botón no optimizado
   - El botón optimizado evita el re-render innecesario

## Instalación y uso

1. Clona este repositorio
2. Abre el archivo `index.html` en tu navegador
3. Abre la consola del navegador para ver los mensajes de log de renderizado

## Demo en vivo

Puedes ver el proyecto funcionando en: [http://awita.site/usuarios/men19644/react-hooks/useCallback](http://awita.site/usuarios/men19644/react-hooks/useCallback)

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
