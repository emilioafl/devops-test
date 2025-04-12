# DevOps Test

Este repositorio actúa como un proyecto padre que incluye dos submódulos de Git:

- `demo-java`
- `pipeline`

Estos submódulos se gestionan mediante la funcionalidad de submódulos de Git.

## 📆 Clonar el Repositorio

Para clonar este repositorio junto con sus submódulos, utiliza el siguiente comando:

```bash
git clone --recurse-submodules https://github.com/emilioafl/devops-test.git
```

Si ya clonaste el repositorio sin la opción `--recurse-submodules`, puedes inicializar y actualizar los submódulos manualmente:

```bash
git submodule update --init --recursive
```

## 🔄 Actualizar los Submódulos

Si los submódulos han sido actualizados (por ejemplo, se han hecho nuevos commits en sus repositorios remotos), puedes obtener los cambios más recientes con:

```bash
git submodule update --remote
```

## 📁 Estructura del Proyecto

```
devops-test/
├── demo-java/
└── pipeline/
```

## 🛠️ Notas

- Los submódulos apuntan a commits específicos. Si realizas cambios dentro de un submódulo, debes hacer commit dentro de él primero. Luego, desde el repositorio padre:

  ```bash
  git add <nombre-submodulo>
  git commit -m "Actualizar referencia del submódulo"
  ```
