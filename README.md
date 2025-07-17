# Repositorio del sitio del curso MISW4406
## Diseño y construcción de soluciones no monolíticas

En este repositorio puede encontrar toda la documentación acerca de tutoriales del curso. Este repositorio usa [Jekyll](https://github.com/BillRaymond/install-jekyll-apple-silicon/blob/main/README.md) para el compilación de archivos `.md` en páginas HTML y CSS. Finalmente, el servidor de documentación se despliega usando [Github Pages](https://pages.github.com/).

### Correr localmente

Si desea correr el servidor localmente ejecute el siguiente comando para instalar todas las dependencias:

```bash
bundle install
```

Una vez con todas las dependencias puede ejectuar el servidor. Si usa el parámetro `--livereload` le va a permitir ir haciendo cambios y verlos en su browser (sin necesidad de tener que parar y correr el servidor con cada nuevo cambio).

```bash
bundle exec jekyll serve --livereload
```

### Uso de devcontainers

Si prefiere un entorno ya configurado, este repositorio incluye soporte para [devcontainers](https://containers.dev){:target="_blank"}.
Puede abrirlo directamente en Codespaces o en Visual Studio Code. El archivo de configuración sugerido es:

```json
{
  "name": "misw4406",
  "image": "mcr.microsoft.com/vscode/devcontainers/python:3.12",
  "features": {
    "ghcr.io/devcontainers/features/docker-in-docker:2": {}
  },
  "postCreateCommand": "bundle install"
}
```

El contenedor se basa en Python 3.12 y ejecuta `bundle install` automáticamente tras su creación.
