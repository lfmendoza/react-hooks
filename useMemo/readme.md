# Filtro de usuarios optimizado con useMemo

## Descripción

Este proyecto implementa un componente de búsqueda de usuarios en React que utiliza el hook useMemo para optimizar el rendimiento al filtrar usuarios. El componente permite buscar usuarios por nombre o descripción, distinguir entre mayúsculas y minúsculas, y agregar nuevos usuarios a la lista.

## Características

- Filtrado de usuarios por nombre o descripción
- Opción para distinguir mayúsculas y minúsculas en la búsqueda
- Formulario para agregar nuevos usuarios
- Optimización del rendimiento mediante useMemo

## Tecnologías utilizadas

- React 18
- Hooks (useState, useMemo)
- Tailwind CSS para estilos
- Babel para compilar JSX

## Implementación

El componente principal UserSearch utiliza:

- `useState` para gestionar el estado de:
  - Lista de usuarios
  - Texto de búsqueda
  - Sensibilidad a mayúsculas/minúsculas
  - Formulario de nuevo usuario
- `useMemo` para optimizar el cálculo de la lista filtrada, que solo se recalcula cuando:
  - Cambia el texto de búsqueda
  - Cambia la lista de usuarios
  - Cambia la configuración de sensibilidad a mayúsculas/minúsculas

## Instalación y uso

1. Clona este repositorio
2. Abre el archivo `index.html` en tu navegador

## Demo en vivo

Proyecto funcionando en: [http://awita.site/usuarios/men19644/react-hooks/useMemo](http://awita.site/usuarios/men19644/react-hooks/useMemo)

## Estructura del proyecto

```
.
├── index.html     # Archivo HTML con CDN de React y código JSX
└── README.md      # Este archivo
```

## Aprendizajes clave

- Uso del hook useMemo para optimizar rendimiento
- Cuándo memorizar cálculos en React
- Manejo de formularios y estados en componentes funcionales
- Implementación de filtros de búsqueda eficientes

## Autor

Fernando Mendoza

## Licencia

MIT
