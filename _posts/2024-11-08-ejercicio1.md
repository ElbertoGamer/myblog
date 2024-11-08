
# Creación de Sitios Web Estáticos con GitHub Pages y Jekyll (1ª Parte)

## Recursos y Temas de Jekyll
- Generadores de páginas estáticas: [jamstack.org](https://jamstack.org/generators/)
- Sitio oficial de Jekyll: [jekyllrb.com](https://jekyllrb.com/)
- Temas de Jekyll:
  - [Página oficial de Jekyll](https://jekyllrb.com/docs/themes/)
  - [Jekyll Themes](http://jekyllthemes.org/)
  - [Free Jekyll Themes](https://jekyllthemes.io/free)
  - [Jamstack Themes](https://jamstackthemes.dev/ssg/jekyll/)

## Características de Jekyll
- Convierte texto plano en páginas web estáticas.
- Es un generador de contenido estático adecuado para blogs y sitios de proyectos.
- Almacena páginas web en HTML o Markdown sin necesidad de bases de datos.
- Escrito en Ruby, distribuido bajo licencia de código abierto.
- Utiliza ficheros Markdown para contenido y YAML para datos, sin tecnología de servidor.

## Requerimientos e Instalación en Debian/Ubuntu
1. **Instala Ruby**: `sudo apt-get install ruby-full build-essential zlib1g-dev`
2. **Configura RubyGems**:
   ```
   echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
   echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
   echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
   source ~/.bashrc
   ```
3. **Instala Jekyll y Bundler**:
   ```
   gem install jekyll bundler
   ```

## Creación de un Sitio Jekyll
1. **Crear repositorio remoto** en GitHub (ej. `myblog`).
2. **Clonar repositorio**:
   ```
   git clone https://github.com/tu_cuenta_github/myblog.git
   ```
3. **Configurar Jekyll**:
   ```
   jekyll new . --force
   ```
   Este comando crea la estructura básica del proyecto.

## Estructura de Carpetas de Jekyll
- `_posts/`: Contenido de blog con formato `YEAR-MONTH-DAY-title.md`.
- `_config.yml`: Archivo de configuración principal en YAML.
- `assets/`: Almacena imágenes y CSS.
- `_includes/`, `_layouts/`, `_sass/`: Fragmentos HTML, plantillas y archivos SCSS para el diseño.
- `_site/`: Contiene el sitio generado por Jekyll.

## Publicar y Visualizar el Sitio
1. **Ejecutar el servidor localmente**:
   ```
   jekyll serve
   # o con Bundler
   bundle exec jekyll serve
   ```
   Navegar en: `http://localhost:4000`
2. **Publicar en GitHub Pages**:
   - Sube el proyecto:
     ```
     git add .
     git commit -m "Subir"
     git push -u origin gh-pages
     ```
   - Activa GitHub Pages en las configuraciones del repositorio y obtén la URL.

## Configuración de Plugins y Temas
En `Gemfile`:
```
# Usa el tema minima
gem "minima", "~> 2.5"
# Activa GitHub Pages
gem "github-pages", group: :jekyll_plugins
```

## Personalización de Contenido
1. **Editar `_config.yml`**:
   - Ajusta `title`, `email`, `description`, `baseurl`, `url`, `twitter`, `github`.
2. **Añadir Páginas**: Crea archivos `.md`.
3. **Crear Publicaciones**: En `_posts/`, usa el formato `YYYY-MM-DD-titulo.md`.

## Ejemplo de Formato Markdown para Páginas y Publicaciones

```
---
layout: page
title: Mi Página Personalizada
permalink: /mi-pagina/
---
```

```
---
layout: post
title: "Mi primera publicación"
date: 2023-10-17
categories: noticias
---
```

## Comandos Finales para Desplegar en GitHub Pages
1. Agrega cambios:
   ```
   git add .
   git commit -m "Hice cambios"
   git push origin gh-pages
   ```
2. Accede al sitio en `https://ElbertoGamer.io/myblog/`.

