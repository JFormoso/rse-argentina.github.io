# Solución: Temas de Bootstrap sobrescribiendo CSS personalizado

## 🔧 El problema

Los temas de Bootstrap (como "united" y "darkly") tienen sus propios colores y estilos que pueden sobrescribir tu CSS personalizado, especialmente los colores.

## ✅ Soluciones disponibles

### Opción 1: Usar tema "default" (Ya implementado)
He cambiado tu configuración a:
```yaml
format:
  html:
    theme: 
      light: default
      dark: default
    css: styles.css
```

El tema "default" es más neutral y permite que tus estilos personalizados tengan prioridad.

### Opción 2: Sin temas de Bootstrap (Máximo control)
Si aún tienes problemas, puedes usar `_quarto-sin-temas.yml`:

1. Renombra el archivo:
   ```bash
   mv _quarto.yml _quarto-con-temas.yml
   mv _quarto-sin-temas.yml _quarto.yml
   ```

2. Este archivo no usa temas de Bootstrap, solo tu CSS personalizado.

### Opción 3: Forzar colores con CSS adicional
Si prefieres mantener los temas, agrega este CSS al inicio de tu `styles.css`:

```css
/* Forzar colores de Bootstrap */
[data-bs-theme="light"] {
  --bs-primary: #702552 !important;
  --bs-secondary: #2c3e50 !important;
  --bs-link-color: #702552 !important;
  --bs-link-hover-color: #2c3e50 !important;
  --bs-body-color: #212529 !important;
}

[data-bs-theme="dark"] {
  --bs-primary: #a87391 !important;
  --bs-secondary: #9b5c7f !important;
  --bs-link-color: #a87391 !important;
  --bs-link-hover-color: #9b5c7f !important;
}
```

## 🎨 Verificar que funciona

1. Renderiza el sitio:
   ```bash
   quarto preview
   ```

2. Verifica estos elementos:
   - Enlaces deben ser púrpura (#702552)
   - Botones principales deben ser púrpura
   - Títulos H1 deben tener borde púrpura
   - Navbar brand debe ser púrpura

## 💡 Tips adicionales

- **Limpiar caché**: A veces necesitas limpiar y reconstruir:
  ```bash
  quarto clean
  quarto preview
  ```

- **Forzar recarga en navegador**: Ctrl+Shift+R (o Cmd+Shift+R en Mac)

- **Inspeccionar elementos**: Usa las herramientas de desarrollo del navegador (F12) para ver qué estilos se están aplicando

## 📝 CSS ya actualizado

Tu `styles.css` ahora incluye:
- `!important` en reglas críticas
- Selectores más específicos
- Variables CSS con prioridad
- Sobrescritura de clases de Bootstrap

¡Esto debería resolver el problema de los temas sobrescribiendo tus colores personalizados!
