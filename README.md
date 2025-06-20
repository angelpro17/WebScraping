# WebScraping.py - PopMart Stock Monitor

Este repositorio contiene un único script **WebScraping.py** para monitorizar precios y stock de productos en PopMart con Selenium.

## Características

* Configuración interactiva por consola y guardado en `popmart_selenium_config.json`.
* Soporta múltiples productos con URL, precio objetivo y opción de auto-agregar al carrito.
* Login automático a PopMart (maneja el modal de ubicación y overlays).
* Detección de stock usando diferentes selectores (`ADD TO BAG`, `ADD TO CART`).
* Envío de alertas por email cuando el producto está en stock o se añade al carrito.
* Modo de ejecución **única** (no continua).

## Requisitos

* Python 3.8 o superior
* Google Chrome instalado
* Librerías Python:

  ```bash
  pip install selenium webdriver-manager
  ```

## Uso

1. Clonar o descargar este repositorio.
2. Asegurarse de estar en la carpeta donde está `WebScraping.py`.
3. Ejecutar el script:

   ```bash
   python WebScraping.py
   ```
4. Seguir el asistente interactivo para:

   * Añadir productos (nombre, URL, precio objetivo, auto-agregar).
   * Configurar login (email y contraseña) si es necesario.
   * Configurar alertas por email (SMTP, credenciales y destinatario).
5. El script realizará una **sólo ejecución** de verificación de stock y luego terminará.

## Archivo de configuración

Tras la primera ejecución se crea `popmart_selenium_config.json`. Puedes editarlo manualmente o volver a ejecutar `WebScraping.py` y optar por reconfigurar para modificar tus ajustes.

## Estructura del repositorio

```
├── WebScraping.py                # Script principal
├── popmart_selenium_config.json  # Configuración (generado tras el primer run)
└── README.md                     # Este archivo de documentación
```

## Licencia

MIT © 2025 Luis Ángel Anampa Lavado
