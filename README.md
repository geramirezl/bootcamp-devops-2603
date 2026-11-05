# Mapa del ciclo DevOps: Caso TiendaNova

## 1. Situación inicial

| # | Problema | Cuándo ocurre | Quién lo arregla |
|---|----------|---------------|------------------|
| 1 | Los despliegues se hacen a mano, una vez al mes | Al publicar cambios | DevOps |
| 2 | Un tercio de los despliegues falla | Antes y durante la publicación | DevOps |
| 3 | No sabemos si la tienda está bien | Cuando ya está en producción | SRE |
| 4 | Cada entorno está configurado distinto | Al preparar los entornos | Platform |
| 5 | Desarrollo y operaciones no hablan | Desde que se planea el trabajo | DevOps |
| 6 | Nadie cuida la seguridad | En todo el ciclo | DevSecOps |

## 2. Solución propuesta

| # | Problema | Qué hacer |
|---|----------|-----------|
| 1 | Despliegues manuales una vez al mes | Publicar automáticamente, en cambios pequeños y frecuentes, en lugar de un lote grande al mes |
| 2 | Un tercio de los despliegues falla | Revisar el código y probar la tienda antes y después de publicar, con vuelta atrás automática si algo falla |
| 3 | No sabemos si la tienda está bien | Tablero con tres indicadores clave (velocidad de carga, errores y disponibilidad) y alertas cuando algo sale mal |
| 4 | Entornos distintos | Usar la misma copia de la aplicación en todos los entornos y cambiar solo la configuración |
| 5 | Desarrollo y operaciones no hablan | Quien crea la función ayuda a cuidarla cuando está en uso; al revisar fallas, buscar qué pasó sin culpar a nadie |
| 6 | Nadie cuida la seguridad | Revisar la seguridad desde la planificación, proteger los pagos y los datos de los clientes (que no aparezcan en logs ni en el código), guardar las contraseñas en un lugar seguro y revisar las librerías externas |

## 3. Prioridad

Primero los problemas 2 y 6, porque sin ellos no conviene publicar con más frecuencia.
