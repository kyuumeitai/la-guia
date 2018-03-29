Git
===

### Commits en Git

Los mensajes de commit:

  * siempre los hacemos en inglés
  * normalmente tienen una sola línea (aunque sabemos que más podría ser mejor)
  * la primera línea se forma de un **tipo**, un **contexto** y una **descripción**
    ```
    tipo(scope/contexto):descripción
    ```

  La línea no debiera tener más de 100 caracteres para que se lea bien en Github.
  En caso de no poder resumir el commit en menos de 100 carácteres, usa un título
  generalizado y especifica en la descripción del commit.
    ```
      git commit -m "titulo" -m "descripción"
    ```

#### Tipo

  * **feat**: Un nuevo feature
  * **fix**: La corrección de un bug
  * **chore**: Cambios al proceso de build y herramientas auxiliares
  * **test**: Agrega tests
  * **style**: Cambios que no afectan el significado del código (espacios, indentación, etc.)

#### Contexto

  El contexto es suele tener una referencia al scope asociado y a una palabra que haga referencia al
  lugar del código donde afecta el commit. En caso de tener más de una palabra, usamos kebab-case.
  Un ejemplo de contexto sería `api/admin-login`.

#### Descripción

  * usamos el verbo imperativo en inglés:  "change" not "changed" nor "changes"
  * sin mayúscula al principio
  * sin punto (.) al final

Nota: Esto es un extracto/traducción de [este documento](https://github.com/ajoslin/conventional-changelog/blob/master/CONVENTIONS.md), que es más completo, pero que por el momento no es una práctica que sigamos completamente en Platanus.

### Branches y Pull-requests

Salvo cosas muy insignificantes, los features los hacemos en un nuevo branch y hacemos un pull-request hacia master.
