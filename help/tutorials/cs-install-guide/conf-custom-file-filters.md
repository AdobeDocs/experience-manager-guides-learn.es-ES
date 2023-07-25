---
title: Configurar filtros para cuadro de diálogo de exploración de archivos
description: Obtenga información sobre cómo configurar filtros para el cuadro de diálogo de exploración de archivos
source-git-commit: 6051181e243cf71919901093c1b5590f21832545
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---


# Configurar filtros para cuadro de diálogo de exploración de archivos {#id20CIL7009GN}

Mientras trabaja en el Editor Web, debe utilizar el cuadro de diálogo de exploración de archivos para insertar elementos como imagen, referencia o referencia de clave. El cuadro de diálogo de exploración de archivos predeterminado no ofrece ninguna opción de filtrado de archivos. Puede añadir sus propios filtros para acceder a los archivos necesarios de forma fácil y rápida.

Realice los siguientes pasos para agregar las opciones de filtrado de archivos personalizadas al cuadro de diálogo de exploración de archivos:

1. Para descargar el archivo de configuración de la interfaz de usuario, inicie sesión en Adobe Experience Manager como administrador.

1. Haga clic en el vínculo Adobe Experience Manager en la parte superior y elija **Herramientas**.
1. Seleccionar **Guías** en la lista de herramientas y haga clic en **Perfiles de carpeta**.
1. Haga clic en **Perfil global** mosaico.
1. Seleccione el **Configuración del editor XML** y haga clic en **Editar** en la parte superior
1. Haga clic en **Descargar** para descargar el archivo ui\_config.json en su sistema local. A continuación, puede realizar cambios en el archivo y luego cargarlo.
1. En el `ui_config.json` , añada la definición de los filtros que desea añadir.

   El siguiente fragmento de código muestra cómo agregar dos opciones de filtrado: archivos DITA y archivos de imagen.

   ```
   "browseFilters": [
                       {
                       "title": "DITA Files",
                       "property": "jcr:content/metadata/dita_class",
                       "operation": "exists"
                       },
                       {
                       "title": "Image Files",
                       "property": "jcr:content/metadata/dc:format",
                       "value": [
                       "image/jpeg",
                       "image/gif",
                       "image/png"
                       ]
                       }
                       ]
   ```

   En el fragmento de código anterior, el primer filtro es para archivos DITA. La definición del filtro toma los siguientes parámetros:

   title : Nombre para mostrar del filtro. Este título aparece como la opción de filtrado en el cuadro de diálogo de exploración de archivos.

   property : La propiedad que debe coincidir en los metadatos del archivo. Por ejemplo, para permitir solo los archivos que tienen el `dita_class` metadatos en su propiedad, el filtro de propiedad toma &quot; `jcr:content/metadata/dita_class`&quot; como su valor.

   operación : especifique &quot; `exists`&quot; para coincidir con la existencia del valor especificado en el parámetro de propiedad.

   El segundo filtro es para archivos de imagen. Los parámetros son similares al primer filtro, excepto el parámetro `value` parámetro. El `value` El parámetro toma una matriz de tipos de imagen como valor. Todos los tipos de archivo especificados en el parámetro value se buscan y se muestran en el cuadro de diálogo de exploración de archivos; el resto de tipos de archivo se omiten.

1. Guarde el *ui\_config.json* y cargar el mismo. A continuación, vuelva a cargar el editor web.

   Al iniciar el cuadro de diálogo de exploración de archivos, se muestran las opciones de filtro configuradas en el archivo ui\_config.json.

   ![](assets/file-browse-custom-filters.png)


**Tema principal:**[ Personalizar editor web](conf-web-editor.md)
