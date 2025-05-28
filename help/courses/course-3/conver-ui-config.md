---
title: Configuración del editor de AEM Guides
description: Personalizar configuraciones de JSON y convertir configuraciones de interfaz de usuario para el nuevo Editor de AEM Guides.
exl-id: bb047962-0e2e-4b3a-90c1-052a2a449628
source-git-commit: efdb02d955e223783fc1904eda8d41942c1c9ccf
workflow-type: tm+mt
source-wordcount: '1197'
ht-degree: 0%

---

# Información general

Al migrar de la IU antigua a la nueva IU de AEM Guides, las actualizaciones de **ui_config** deben convertirse a configuraciones de IU más flexibles y modulares. Este marco ayuda a adoptar cambios sin problemas en **editor_toolbar** y [otras barras de herramientas](/help/courses/course-3/conver-ui-config.md#editing-json-for-different-screens). El proceso también admite la modificación de otras vistas y widgets de la aplicación.

>[!NOTE]
>
>Las personalizaciones aplicadas a botones específicos pueden tener problemas durante la transición al marco de trabajo de extensión. Si esto sucede, puede generar un ticket de asistencia con referencia a esta página para obtener asistencia y resolución rápidas.

## Edición de JSON para diferentes pantallas

Los archivos JSON se pueden agregar a la sección Configuración de la interfaz de usuario del Editor XML para varias pantallas y widgets. A continuación se muestra una lista de los widgets más utilizados y sus ID:

1. [editor_toolbar](assets/toolbars/editor_toolbar.json): barra de herramientas del editor web que consta de acciones de archivo y contenido.
1. [editor_tab_bar](assets/toolbars/editor_tab_bar.json): La vista con fichas de los archivos abiertos en el editor web tiene acciones que se pueden realizar en los archivos abiertos.
1. [file_mode_switcher](assets/toolbars/file_mode_switcher.json): ayuda a cambiar entre los diferentes modos disponibles (autor, origen y vista previa) para los archivos abiertos en webeditor.

   ![barra de herramientas del editor](images/reuse/editor_toolbar.png)

1. [map_console_navigation_bar](assets/toolbars/map_console_navigation_bar.json): Es la barra de información del mapa abierto en la consola de mapas. Permite cambiar el mapa y proporciona acceso a la configuración.
1. [map_console_action_bar](assets/toolbars/map_console_action_bar.json): Esta es la barra de acciones para los elementos de la consola de mapas, como Ajuste preestablecido de salida, Línea de base, Traducción e Informes, que proporciona información relevante junto con sus respectivos botones de acción.

   ![map_console](images/reuse/map_console.png)

1. [home_navigation_bar](assets/toolbars/home_navigation_bar.json): barra de encabezado de la página principal de las guías donde se muestra el mensaje de bienvenida junto con el perfil de carpeta seleccionado.

   ![barra_navegación_inicio](images/reuse/home_navigation_bar.png)

<br>

## Estructura general de cada JSON

Cada JSON sigue una estructura coherente:

1. `id`: especifica el widget donde se personaliza el componente.
1. `targetEditor`: define cuándo mostrar u ocultar un botón mediante las propiedades de modo y editor:

   Se admiten las siguientes opciones en `targetEditor`:

   - `mode`
   - `displayMode`
   - `editor`
   - `documentType`
   - `documentSubType`
   - `flag`

   Para obtener más información, vea [Descripción de las propiedades de targetEditor](#understanding-targeteditor-properties)

   >[!NOTE]
   >
   > La versión de 2506 de Experience Manager Guides presenta nuevas propiedades: `displayMode`, `documentType`, `documentSubType` y `flag`. Estas propiedades solo son compatibles a partir de la versión 2506. Del mismo modo, el cambio de `toc` a `layout` en la propiedad de modo también se aplica a partir de esta versión.
   >
   > Ahora hay disponible un nuevo campo, `documentType`, junto con el campo `editor` existente.  Ambos campos son compatibles y se pueden utilizar según sea necesario. Sin embargo, se recomienda usar `documentType` para garantizar la coherencia en todas las implementaciones, especialmente cuando se trabaja con la propiedad `documentSubType`. El campo `editor` sigue siendo válido para admitir la compatibilidad con versiones anteriores y las integraciones existentes.


1. `target`: especifica dónde se agregará el nuevo componente. Esto utiliza pares o índices de clave-valor para la identificación única. Los estados de vista incluyen:

   - **anexar**: agregue al final.

   - **prepend**: agregue al principio.

   - **reemplazar**: reemplace un componente existente.

Ejemplo de estructura JSON:

```json
{
  "id" : "editor_toolbar",
  "view": {
    "items": [
      {
        ...,
        "targetEditor": {
          "mode": [
            "preview"
          ],
          "editor": [
            "xml"
          ]
        },
        "target": {
          "key": "label",
          "value": "Table",
          "viewState": "prepend"
        },
        ...
      },
    ]
  }
}
```

<br>

## Explicación de las propiedades `targetEditor`

A continuación se muestra un desglose de cada propiedad, su propósito y los valores admitidos.

### `mode`

Define el modo operativo del editor.

**Valores compatibles**: `author`, `source`, `preview`, `layout` (anteriormente `toc`), `split`

### `displayMode` *(opcional)*

Controla la visibilidad o la interactividad de los componentes de la IU. Si no se especifica, el valor predeterminado se establece en `show`.

**Valores compatibles**: `show`, `hide`, `enabled`, `disabled`

Ejemplo:

```
 {
        "icon": "textBulleted",
        "title": "Custom Insert Bulleted",
        "on-click": "$$AUTHOR_INSERT_REMOVE_BULLETED_LIST",
        "key": "$$AUTHOR_INSERT_REMOVE_BULLETED_LIST",
        "targetEditor": {
          "documentType": [
            "ditamap"
          ],
          "mode": [
            "author"
          ],
          "displayMode": "hide"
        }
      },
```

### `editor`

Especifica el tipo de documento principal en el editor.

**Valores compatibles**: `ditamap`, `bookmap`, `subjectScheme`, `xml`, `css`, `translation`, `preset`, `pdf_preset`

### `documentType`

Indica el tipo de documento principal.

**Valores compatibles**: `dita`, `ditamap`, `bookmap`, `subjectScheme`, `css`, `preset`, `ditaval`, `reports`, `baseline`, `translation`, `html`, `markdown`, `conditionPresets`

> Pueden admitirse valores adicionales para casos de uso específicos.

Ejemplo:

```
 {
        "icon": "textNumbered",
        "title": "Custom Numbered List",
        "on-click": "$$AUTHOR_INSERT_REMOVE_NUMBERED_LIST",
        "key": "$$AUTHOR_INSERT_REMOVE_NUMBERED_LIST",
        "targetEditor": {
          "documentType": [
            "dita",
            "ditamap"
          ],
          "mode": [
            "author",
            "source"
          ]

        }
      },
```

### `documentSubType`

Clasifica el documento en función de `documentType`.

- **Para`preset`**: `pdf`, `html5`, `aemsite`, `nativePDF`, `json`, `custom`, `kb`
- **Para`dita`**: `topic`, `reference`, `concept`, `glossary`, `task`, `troubleshooting`

> Pueden admitirse valores adicionales para casos de uso específicos.

Ejemplo:

```
 {
        "icon": "rename",
        "title": "Custom Rename",
        "on-click": "$$PUBLISH_PRESETS_RENAME",
        "label": "Custom Rename",
        "key": "$$PUBLISH_PRESETS_RENAME",
        "targetEditor": {
          "documentType": [
            "preset"
          ],
          "documentSubType": [
            "nativePDF",
            "aemsite",
            "json"
          ]

        }
      },
```

### `flag`

Indicadores booleanos para el estado o las capacidades del documento.

**Valores compatibles**: `isOutputGenerated`, `isTemporaryFileDownloadable`, `isPDFDownloadable`, `isLocked`, `isUnlocked`, `isDocumentOpen`

Además, también puede crear una marca personalizada dentro de `extensionMap` que se utiliza como marca en `targetEditor`. En este caso, `extensionMap` es una variable global que se usa para agregar claves personalizadas o valores observables.

Ejemplo:

```
 {
        "icon": "filePDF",
        "title": "Custom Export pdf",
        "on-click": "$$DOWNLOAD_TOPIC_PDF",
        "key": "$$DOWNLOAD_TOPIC_PDF",
        "targetEditor": {
          "documentType": [
            "markdown"
          ],
          "mode": [
            "preview"
          ],
          "flag": ["isPDFDownloadable"]

        }
      },
```


## Ejemplos

A continuación se muestra un ejemplo de cómo agregar, eliminar o reemplazar un botón en la barra de herramientas del editor.

### Adición de un botón

Agregando un nuevo botón **Insertar tabla personalizada** en **editor_toolbar** para agregar una tabla simple que solo está visible en el modo de vista previa.

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "icon": "table",
        "title": "Insert Custom Table",
        "on-click": {
          "name": "$$AUTHOR_INSERT_ELEMENT",
          "args": [
            "simpletable",
            "table",
            "choicetable"
          ]
        },
        "key": "$$AUTHOR_INSERT_ELEMENT",
        "targetEditor": {
          "mode": [
            "preview"
          ],
        },
        "target": {
          "key": "label",
          "value": "Table",
          "viewState": "prepend"
        }
      }
    ]
  }
}
```

![Insertar tabla personalizada](images/reuse/insert-custom-table.png)

### Eliminación de un botón

Eliminación de un botón de la barra de herramientas. Aquí eliminamos el botón Añadir imagen de la barra de herramientas del editor.

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "hide": true,
        "target": {
          "key": "label",
          "value": "Image",
          "viewState": "replace"
        }
      }
    ]
  }
}
```

### Reemplazar un botón

Se ha reemplazado el botón **Multimedia** de la barra de herramientas por el botón de inserción de vínculos **Youtube**, que solo está visible en el modo de creación.

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "icon": "s2youtube",
        "title": "Youtube",
        "on-click": {
          "name": "$$AUTHOR_INSERT_ELEMENT",
          "args": "<object data='http://youtube.com'></object>"
        },
        "targetEditor": {
          "mode": [
            "author"
          ]
        },
        "target": {
          "key": "elementId",
          "value": "toolbar-multimedia",
          "viewState": "replace"
        }
      }
    ]
  }
}
```

![Botón de YouTube](images/reuse/youtube-button.png)

<br>

### Adición de un botón en el modo de vista previa

De acuerdo con el diseño, la visibilidad del botón se administra por separado para los modos bloqueado y desbloqueado (solo lectura) para mantener una experiencia de usuario clara y controlada. De forma predeterminada, cualquier botón recién agregado está oculto cuando la interfaz está en modo de solo lectura.
Para que un botón esté visible en modo **solo lectura**, debe especificar un destino que lo coloque en una subsección de la barra de herramientas a la que se pueda acceder incluso cuando la interfaz esté bloqueada.
Por ejemplo, si especifica el destino como **Descargar como PDF**, puede asegurarse de que el botón aparece en la misma sección que un botón visible existente, por lo que es accesible en modo desbloqueado.

```json
"target": {
  "key": "label",
  "value": "Download as PDF",
  "viewState": "prepend"
}
```

Agregando un botón **Exportar como PDF** en el modo de **vista previa** que será visible tanto en el modo de bloqueo como de desbloqueo.

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "icon": "filePDF",
        "title": "Export as PDF",
        "on-click": "$$DOWNLOAD_TOPIC_PDF",
        "key": "$$DOWNLOAD_TOPIC_PDF",
        "targetEditor": {
          "editor": [
            "ditamap",
            "xml"
          ],
          "mode": [
            "preview"
          ]
        },
        "target": {
          "key": "label",
          "value": "Download as PDF",
          "viewState": "prepend"
        }
      },
      {
        "icon": "filePDF",
        "title": "Export as PDF",
        "on-click": "$$DOWNLOAD_TOPIC_PDF",
        "key": "$$DOWNLOAD_TOPIC_PDF",
        "targetEditor": {
          "editor": [
            "ditamap",
            "xml"
          ],
          "mode": [
            "preview"
          ]
        }
      }
    ]
  }
}
```

El siguiente fragmento muestra el botón **Exportar como PDF** con escenario de bloqueo.

![Exportar como PDF](images/reuse/lock.png)

Además, el botón **Exportar como PDF** con el escenario de desbloqueo se puede ver en el siguiente fragmento.

![Exportar como PDF](images/reuse/unlock.png)

## Cómo cargar archivos JSON personalizados

1. En la ficha **Configuración del editor XML**, haga clic en **Editar** en la barra superior.
1. Ahora, en la subsección **Configuración de la interfaz de usuario del editor XML**, podrá ver un botón **cargar**.

   ![Botón de carga](images/reuse/ui-config-upload.png){width="400" height="150"}

1. Puede hacer clic en y cargar el json modificado. (El json que se va a cargar debe tener el mismo nombre que el ID del widget que se va a personalizar)
1. Una vez cargado, pulsa **Guardar** en la barra superior.

   Para cada archivo cargado también puede **eliminar** el json para eliminar su personalización de la interfaz de usuario o **descargar** para verlo o modificarlo de nuevo.

   ![Botón de descarga](images/reuse/download-delete-json.png){width="400" height="150"}

<br>


## Cómo cargar CSS personalizado

También puede agregar css para personalizar el aspecto de los botones personalizados añadidos o de los widgets o botones ya existentes en la interfaz de usuario.

Para un botón personalizado recién agregado, agrega una **extraclass** al botón o componente personalizado dentro del JSON.
Para una clase antigua, también se puede inspeccionar element y modificar las clases existentes.

```json
{
  "icon": "table",
  "title": "Insert Custom Table",
  "extraclass": "custom-css",
  "key": "$$AUTHOR_INSERT_ELEMENT",
  "targetEditor": {
    "mode": [
      "preview"
    ],
  },
  "target": {
    "key": "label",
    "value": "Table",
    "viewState": "prepend"
  }
}
```

1. En la ficha **Configuración del editor XML**, haga clic en **Editar** en la barra superior.
1. Ahora, en la subsección **Diseño de página del editor XML**, verá un botón **cargar**.

   ![Botón de carga](images/reuse/page-layout-upload.png){width="400" height="150"}

1. Puede hacer clic en y cargar el css modificado. (Solo se admiten archivos css)
1. Una vez cargado, pulsa **Guardar** en la barra superior.

   Para cada archivo cargado, también puede **eliminar** el css para eliminar su personalización de la interfaz de usuario o **descargar** para verlo o modificarlo de nuevo.

   ![Botón de descarga](images/reuse/download-delete-css.png){width="400" height="150"}


<br>

### Ejemplo para personalizar el botón css

Aquí agregamos un nuevo botón **Insertar tabla personalizada** en **editor_toolbar** para agregar una tabla simple que solo está visible en el modo de vista previa y aplicar un css personalizado en ella.
Este css modifica el fondo del botón y el tamaño de fuente de su título.

![Ejemplo de CSS](images/reuse/css-customization.png)


```css
#editor_toolbar {
  .custom-css {
    background-color: burlywood;
    font-size: 2rem;  
  }
}
```

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "icon": "table",
        "title": "Insert Custom Table",
        "extraclass": "custom-css",
        ...
      }
    ]
  }
}
```

<br>

## Pasos para convertir la configuración de iu en Json modulares

1. En la pantalla Navegación, haga clic en el icono [!UICONTROL **Herramientas**].

   ![Icono de herramientas](images/reuse/tools.png)

1. Seleccione **Guías** en el panel izquierdo.

1. Haga clic en el mosaico [!UICONTROL **Perfiles de carpeta**].

   ![Perfiles de carpeta](images/reuse/folder-profiles-tile.png)

1. Seleccione un perfil de carpeta.

1. Haga clic en la ficha [!UICONTROL **Configuración del editor XML**].

1. Puede hacer clic en el botón **Convertir configuración de interfaz de usuario a JSON**. Esto generará el json **editor_toolbar** y **map_console_action_bar** que contiene los cambios realizados en **ui_config**.

   ![Convertir configuración de interfaz de usuario a JSON](images/reuse/convert-ui-config-json.png)

1. Puede desproteger los json generados de ejemplo para [Editor toolbar](assets/editor_toolbar.json) y [Map console action bar](assets/map_console_action_bar.json)


>[!NOTE]
>
>Los cambios realizados en las secciones **toolbar** y **topbar** se han agregado en el json **editor_toolbar**, que se puede ver en la página Editor. Los cambios que se realizan en los botones relacionados con los ajustes preestablecidos o la traducción en **ui_config** se agregan al json **map_console_action_bar**, que se puede ver en la página Consola de mapa.
