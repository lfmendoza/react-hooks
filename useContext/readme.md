# Tema Claro/Oscuro con useContext

## Descripción

Este proyecto implementa un sistema de cambio de tema (claro/oscuro) utilizando el hook useContext de React. La aplicación demuestra cómo compartir estado global entre componentes sin necesidad de prop drilling (pasar props a través de múltiples niveles de componentes).

## Fundamentos de useContext

useContext es un hook de React que permite:

- Crear un "almacén compartido" de datos accesible desde cualquier componente
- Evitar el prop drilling (pasar props a través de múltiples niveles)
- Compartir estado y funciones de forma global y eficiente
- Actualizar componentes cuando el contexto cambia

## Componentes Implementados

### 1. ThemeContext

- Creado con `createContext()`
- Sirve como el "contenedor" para los datos compartidos

### 2. ThemeProvider

- Componente que envuelve la aplicación
- Proporciona el estado y las funciones a todos los componentes descendientes
- Gestiona el estado `darkMode` y la función `toggleTheme`

### 3. ThemeToggle

- Botón que permite cambiar entre modo claro y oscuro
- Consume el contexto usando `useContext(ThemeContext)`
- Cambia dinámicamente su apariencia según el tema actual

### 4. ThemeDisplay

- Componente que muestra visualmente el tema actual
- Consume el contexto usando `useContext(ThemeContext)`
- Adapta sus estilos según el valor de `darkMode`

### 5. NestedComponent

- Componente anidado que demuestra el acceso al contexto a cualquier nivel
- Muestra cómo evitar el prop drilling al acceder directamente al contexto

## Conceptos Clave Demostrados

### Provider

- Componente que hace disponible el contexto a sus descendientes
- Define qué datos y funciones estarán disponibles
- Se coloca en un nivel alto del árbol de componentes

### Consumer (useContext)

- Hook que permite a los componentes acceder al contexto
- Simplifica el acceso al contexto comparado con Context.Consumer
- Permite suscribirse a cambios en el contexto

## Casos de Uso de useContext

- Temas de aplicación (como se muestra en este ejemplo)
- Autenticación y datos de usuario
- Preferencias de idioma
- Configuraciones de aplicación
- Estado global que muchos componentes necesitan

## Instalación y uso

1. Clona este repositorio
2. Abre el archivo `index.html` en tu navegador
3. Prueba a cambiar entre los modos claro y oscuro con el botón

## Demo en vivo

Puedes ver el proyecto funcionando en: [http://awita.site/usuarios/men19644/react-hooks/useContext](http://awita.site/usuarios/men19644/react-hooks/useContext)

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
