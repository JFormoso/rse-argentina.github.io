# RSE Argentina - Sitio Web

Este es el repositorio del sitio web de RSE Argentina (Research Software Engineering Argentina), construido con [Quarto](https://quarto.org/).

## 🚀 Inicio rápido

### Prerrequisitos

- [Quarto](https://quarto.org/docs/get-started/) (versión 1.3 o superior)
- [Git](https://git-scm.com/)
- Editor de texto (recomendamos VS Code con la extensión de Quarto)

### Instalación

1. Clona el repositorio:
```bash
git clone https://github.com/rse-argentina/website.git
cd website
```

2. Renderiza el sitio localmente:
```bash
quarto preview
```

El sitio estará disponible en `http://localhost:4000`

## 📁 Estructura del proyecto

```
rse-argentina/
├── _quarto.yml          # Configuración principal del sitio
├── index.qmd            # Página principal
├── quienes-somos.qmd    # Página del equipo
├── eventos.qmd          # Página de eventos
├── recursos.qmd         # Página de recursos
├── contacto.qmd         # Página de contacto
├── codigo-conducta.qmd  # Código de conducta
├── styles.css           # Estilos personalizados
├── images/              # Imágenes del sitio
├── docs/                # Sitio renderizado (no editar)
└── README.md            # Este archivo
```

## ✏️ Cómo contribuir

### Agregar o editar contenido

1. Crea una rama nueva:
```bash
git checkout -b feature/mi-contribucion
```

2. Edita los archivos `.qmd` correspondientes
3. Previsualiza tus cambios:
```bash
quarto preview
```

4. Commit y push:
```bash
git add .
git commit -m "Descripción de los cambios"
git push origin feature/mi-contribucion
```

5. Abre un Pull Request en GitHub

### Agregar un evento

Edita el archivo `eventos.qmd` y agrega tu evento siguiendo el formato existente:

```markdown
### Título del evento
📅 **Fecha**: DD de mes de YYYY, HH:MM hs (UTC-3)  
📍 **Modalidad**: Virtual/Presencial  
🎯 **Dirigido a**: Audiencia objetivo

Descripción breve del evento.

[Link de inscripción](https://ejemplo.com)
```

### Agregar un recurso

Edita el archivo `recursos.qmd` y agrega el recurso en la sección correspondiente:

```markdown
- 📚 **[Nombre del recurso](https://link.com)** - Descripción breve
```

## 🎨 Personalización

### Cambiar colores

Los colores del sitio están definidos en `styles.css`. Modifica las variables CSS:

```css
:root {
  --rse-primary: #2c3e50;
  --rse-secondary: #3498db;
  --rse-accent: #e74c3c;
  /* ... */
}
```

### Cambiar el tema

En `_quarto.yml`, puedes cambiar los temas de Bootstrap:

```yaml
format:
  html:
    theme: 
      light: flatly    # Temas: cosmo, flatly, journal, etc.
      dark: darkly     # Temas: darkly, solar, etc.
```

## 🚀 Despliegue

### GitHub Pages (Recomendado)

1. En GitHub, ve a Settings → Pages
2. Selecciona "Deploy from a branch"
3. Elige la rama `main` y carpeta `/docs`
4. Guarda y espera unos minutos

El sitio estará en: `https://rse-argentina.github.io/`

### Despliegue manual

1. Construye el sitio:
```bash
quarto render
```

2. Los archivos estáticos estarán en la carpeta `docs/`
3. Sube esta carpeta a tu servidor web

## 📋 Mantenimiento

### Tareas regulares

- **Mensual**: Actualizar eventos pasados y próximos
- **Trimestral**: Revisar y actualizar recursos
- **Anual**: Actualizar información del equipo y estadísticas

### Comandos útiles

```bash
# Limpiar archivos generados
quarto clean

# Renderizar solo una página
quarto render archivo.qmd

# Verificar links rotos
# (requiere instalar linkchecker)
linkchecker http://localhost:4000
```

## 🐛 Solución de problemas

### El sitio no se renderiza

1. Verifica que Quarto esté instalado:
```bash
quarto --version
```

2. Limpia y vuelve a renderizar:
```bash
quarto clean
quarto render
```

### Los cambios no se ven en GitHub Pages

1. Verifica que hayas hecho push a la rama correcta
2. Espera 5-10 minutos para que GitHub procese los cambios
3. Limpia la caché del navegador (Ctrl+F5)

## 📞 Soporte

Si tienes problemas o preguntas:

- Abre un [issue en GitHub](https://github.com/rse-argentina/website/issues)
- Escribe a: webmaster@rse-argentina.org
- Únete a nuestro [Slack](https://rse-argentina.slack.com)

## 📄 Licencia

Este sitio está bajo licencia [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Eres libre de compartir y adaptar el material, dando crédito apropiado.

## 🙏 Agradecimientos

- [Quarto](https://quarto.org/) por el excelente framework
- [RSE Chile](https://rse-chile.github.io/) por la inspiración
- Todos los miembros de la comunidad RSE Argentina

---

**Última actualización**: Enero 2025
