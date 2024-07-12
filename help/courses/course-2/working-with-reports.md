---
title: Uso de informes
description: Trabajar con informes en  [!DNL Adobe Experience Manager Guides]
exl-id: 755506a6-c416-4a8c-8359-8db7e63a90a4
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 0%

---

# Uso de informes

La pestaña Informes del tablero de mapas permite identificar y resolver vínculos rotos, contenido al que se hace referencia y que se vuelve a utilizar (conrefs), referencias cruzadas u otra información que falte.

>[!VIDEO](https://video.tv.adobe.com/v/339039?quality=12&learn=on)

## Preparación para el ejercicio

Puede descargar archivos de ejemplo para el ejercicio aquí.

[Ejercicio-descarga](assets/exercises/working-with-reports.zip)

## Cargando Assets

1. En Vista de repositorio, seleccione el icono de puntos suspensivos de la carpeta principal para abrir el menú Opciones.

   ![elipses-9.png](images/ellipses-9.png)

1. Seleccione **[!UICONTROL Cargar Assets]**.

   ![upload-assets.png](images/upload-assets.png)

1. Seleccione los archivos que desee cargar en la carpeta y seleccione **Cargar**.

Los ficheros DITA se abrirán y deberá revisarlos para detectar problemas con contenido, conrefs o referencias cruzadas que falten.

## Creación de un mapa

1. Seleccione el icono de puntos suspensivos de la carpeta principal para abrir el menú Opciones.

   ![elipses-9.png](images/ellipses-9.png)

1. Seleccione **Crear > Mapa**.

   ![create-map.png](images/create-map.png)

   Aparece el cuadro de diálogo Crear nuevo mapa.

1. En el campo Plantilla, seleccione **Bookmap** (o **Map** según el tipo de contenido que esté creando) del menú desplegable y asigne un título al mapa.

1. Seleccione **Crear**.

El mapa se crea y el carril izquierdo cambia automáticamente de la vista Repositorio a la vista Mapa.

## Inserción de componentes de mapa

1. Seleccione el icono de lápiz en el carril izquierdo.
Este es el icono Editar y le permite abrir el mapa en el editor.

   ![edit-map.png](images/edit-map.png)

1. Vuelva a la vista Repositorio seleccionando el icono Repositorio.

   ![botón-repositorio.png](images/repository-button.png)

1. Añada un tema al mapa arrastrándolo y soltándolo desde el Repositorio al mapa en el editor.
El indicador de línea le mostrará dónde se colocará el tema.

1. Siga agregando temas según sea necesario.

1. Cuando termine, seleccione **Guardar como nueva versión.**

   ![save-as-new-version.png](images/save-as-new-version.png)

1. En el campo *Comentarios para la nueva versión*, escriba un comentario descriptivo.

1. Seleccione **Guardar**.

## AEM Generación de una salida del sitio de

1. En el Repositorio, seleccione el icono de puntos suspensivos del mapa para abrir el menú Opciones y, a continuación, **Abrir panel de mapas.**

   ![open-map-dashboard.png](images/open-map-dashboard.png)

   El tablero de mapas se abre en otra pestaña.
1. AEM En la pestaña Ajustes preestablecidos de salida, seleccione **Sitio de la**.

   ![aem-site-checkbox](images/aem-site-checkbox.png)

1. Seleccione **Generar**.

1. Vaya a la página Resultados para ver el estado de los resultados generados.
Si hay errores, la pestaña Salidas puede mostrar un círculo naranja debajo de la columna Configuración de generación en lugar de verde, lo que indica que la generación ha finalizado.

1. Seleccione el vínculo en la columna Configuración de generación para abrir la salida generada.
Revise el resultado para ver si falta contenido.

## La pestaña Informes

La pestaña Informes muestra un resumen del tema y una tabla que contiene información del tema y los problemas dentro del mapa.

Lo ideal es comprobar siempre los informes para ver si hay un mapa después de importar el contenido.

![informes.png](images/reports.png)

La columna Elementos que faltan indica el número de imágenes que faltan y de conrefs rotos. Puede seleccionar el icono **Lápiz** para abrir el tema en el editor.

## Resolución de imágenes faltantes

Si faltan imágenes en los archivos, una causa común podría ser que el contenido se haya cargado, pero las imágenes no. Si es así, resuelva los problemas de imágenes que faltan cargando imágenes en una carpeta específica que coincida con la ruta y los nombres de archivo esperados por los archivos.

1. En *Vista de repositorio*, seleccione el icono de puntos suspensivos de la carpeta de imágenes para abrir el menú Opciones.

   ![image-ellipsis.png](images/image-ellipsis.png)

1. Seleccione **[!UICONTROL Cargar Assets]** y seleccione las imágenes que faltan.

1. Seleccione **Cargar**.

Se han cargado las imágenes que faltan. AEM Ahora, una salida del sitio de la nueva generación de datos mostrará estas imágenes, y la pestaña Informes ya no mostrará ningún error de imagen que falte.

## Resolución de congresistas rotos

Si el contenido al que se hace referencia en otra parte (una conref) está vinculado a un archivo dentro de otra carpeta (por ejemplo, uno llamado &quot;reutilizar&quot;). y el contenido no se ha cargado, se debe resolver un error. Por ejemplo, debe crear una subcarpeta llamada &quot;reutilizar&quot; y cargar el archivo que falta en &quot;reutilizar&quot;.

### Cargando un recurso con la interfaz de usuario de [!UICONTROL Assets]

Además de la opción [!UICONTROL Cargar Assets], puede cargar recursos arrastrándolos y soltándolos en la interfaz de usuario de Assets.

1. En Vista de repositorio, seleccione el icono de puntos suspensivos de la carpeta de reutilización para abrir el menú Opciones.

   ![reuse-ellipsis.png](images/reuse-ellipsis.png)

1. Seleccione **Ver en la IU de Assets**.

   ![assets_ui.png](images/assets_ui.png)

1. Arrastre y suelte el archivo en la carpeta.
El archivo se cargará y se resolverá el error de referencia.

Todos los errores se han resuelto. AEM La página Informes indicará que no hay más errores y la generación de un sitio de informes da como resultado una salida completa sin componentes que falten.
