---
name: photo-identity-lock
description: Edición conservadora de fotografías para quitar turistas u objetos sin cambiar caras, cuerpos, ropa, encuadre ni reflejos. Usa máscaras de eliminación y protección, inpainting localizado y verificación de píxeles originales.
---
# Photo Identity Lock

## Reglas
1. Trabajar exclusivamente sobre la fotografía original. Nunca regenerar la escena completa ni recortar sin autorización.
2. Marcar dos máscaras: `protect` para personas y reflejos inmutables y `remove` para objetos a borrar. Nunca superponerlas.
3. Usar un motor de inpainting localizado como IOPaint/LaMa exclusivamente dentro de `remove`. No presentar un editor de máscaras como si incluyera ese motor.
4. Recuperar del original todos los píxeles fuera de `remove`, incluidos todos los píxeles de `protect`.
5. Rechazar resultados que cambien un solo píxel fuera de la zona autorizada, deformen líneas del fondo o creen artefactos.
6. Entregar resultado y límites reales; si no existe motor accesible, entregar máscaras y explicar que la eliminación no está hecha.

## Uso desde iPhone
El editor web permite subir la foto, pintar máscaras y exportarlas. El motor de reconstrucción de fondo requiere integración posterior. No subir fotos privadas a un repositorio público.
