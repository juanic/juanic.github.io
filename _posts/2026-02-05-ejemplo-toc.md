---
title: "Ejemplo de Post con Índice (TOC)"
date: 2026-02-05
categories:
  - Tutorial
tags:
  - jekyll
  - toc
  - guia
layout: single
toc: true
toc_sticky: true
---

Este es un ejemplo de cómo se ve un post con **Tabla de Contenidos (TOC)** lateral.

Jekyll genera automáticamente el índice basándose en los encabezados (títulos) del contenido.

## ¿Cómo funciona?

Simplemente debes agregar `toc: true` en el encabezado (front matter) del archivo markdown.

```yaml
---
title: "Mi Post"
toc: true
toc_sticky: true
---
```

Si quieres que el menú acompañe el scroll, usa `toc_sticky: true`.

## Sección 1: Introducción

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

### Subtítulo 1.1

Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

### Subtítulo 1.2

Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.

## Sección 2: Desarrollo

Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

### Características Principales

1.  **Automático**: No tienes que escribir el índice a mano.
2.  **Responsivo**: Se adapta a diferentes pantallas.
3.  **Navegable**: Permite saltar rápidamente a las secciones.

## Sección 3: Conclusión

Con esta funcionalidad, tus artículos largos serán mucho más fáciles de leer.
