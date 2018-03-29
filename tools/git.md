Git
===

### Commits en Git

Los mensajes de commit:

  * siempre los hacemos en inglés
  * normalmente tienen una sola línea (aunque sabemos que más podría ser mejor)
  * la primera línea se forma de un **tipo**, un **contexto** y una **descripción**
    ```
    tipo(contexto):descripción
    ```

  La línea no debiera tener más de 100 caracteres para que se lea bien en Github.

#### Tipo

  * **feat**: Un nuevo feature
  * **fix**: La corrección de un bug
  * **chore**: Cambios al proceso de build y herramientas auxiliares
  * **test**: Agrega tests
  * **style**: Cambios que no afectan el significado del código (espacios, indentación, etc.)

#### Contexto

El contexto es una palabra que hace referencia al lugar del código o funcionalidad que afecta el commit. Debe escribirse usando `kebab-case`, por ejemplo: `user-signup`

De manera opcional, se puede agregar información sobre el componente específico del código afectado. Si se agrega esta información:

  * Debe ir después del contexto, separado usando un punto (`.`). Por ejemplo: `api.LoginService`
  * El nombre del componente modificado debe estar en el mismo formato en el que aparece en el código (por ejemplo en `CamelCase` si es una clase ruby).

#### Descripción

  * usamos el verbo imperativo en inglés:  "change" no "changed" ni "changes"
  * sin mayúscula al principio
  * sin punto (.) al final

Nota: Esto es un extracto/traducción de [este documento](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#commits), que es más completo, pero que por el momento no es una práctica que sigamos completamente en Platanus

### Branches y Pull-requests

Salvo cosas muy insignificantes, los features los hacemos en un nuevo branch y hacemos un pull-request hacia master.

### Ejemplo

Como ejemplo de estas recomendaciones el siguiente commit soluciona un bug en el componente/clase `SignUpForm` del frontend de una aplicación, en el cual no se estaba entregando feedback de la validación sobre si el nombre de usuario estaba disponible o no:

```
fix(ui.SignUpForm): validate username availability

The `SignUpForm` component wasn´t validating the availability of the `username` field and only displayed a `couldn´t create account` error on submit.

This commit adds an asynchronous validation when typing on the field so the user will know if the username is available before completing further fields.
```
