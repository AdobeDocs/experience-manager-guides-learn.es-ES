---
title: Flujos de trabajo de creación de contenido simples
description: Creación de contenido en AEM Guides
exl-id: e4b8e512-0688-44f7-b981-78af33b57b08
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 1%

---

# Flujos de trabajo de creación de contenido simple

El editor de AEM Guides tiene varios métodos abreviados que simplifican el flujo de trabajo de creación de contenido. Estos métodos abreviados permiten a los usuarios agregar y modificar rápidamente imágenes, trabajar con varios temas a la vez, corregir errores, descargar PDF de temas y trabajar con versiones y rótulos.

>[!VIDEO](https://video.tv.adobe.com/v/342770?quality=12&learn=on)

## Añadir una imagen

Las imágenes se pueden agregar directamente desde una unidad local.

1. Arrastre y suelte la imagen directamente en el tema. Aparecerá el cuadro de diálogo **Cargar Assets**.

   ![Cuadro De Diálogo Cargar Assets](images/lesson-15/upload-assets-dialog.png)

1. Modifique la ruta de la carpeta a la ubicación de imagen deseada.

1. Cambie el nombre de la imagen por algo representativo de su propósito.

1. Haga clic en [!UICONTROL **Cargar**]. 

## Modificación de una imagen

1. Cambiar el tamaño de una imagen arrastrando y soltando una esquina.

1. Para mover una imagen a otra ubicación dentro del tema, arrástrela y suéltela.

1. Use **Propiedades de contenido** en el panel derecho para modificar las propiedades de una imagen

   - desconchar

   - position

   - alineación, o

   - otros atributos.

   ![Propiedades de contenido](images/lesson-15/content-properties.png)

## Trabajar con varios temas

La vista dividida es útil cuando se comparan temas, se copian y se pegan entre temas, o se arrastra y se suelta contenido de un tema a otro.

1. Abra dos o más temas relacionados.

1. Haga clic en la pestaña Título de un archivo para abrir el menú contextual.

1. Seleccione [!UICONTROL **Split**].

1. Elija **derecho**.

   ![Vista dividida](images/lesson-15/split-view.png)

## Corrección de errores tipográficos

1. Busque la palabra o frase que contiene el error.

1. Mantenga presionado [!UICONTROL **Ctrl**].

1. Haga clic con el botón secundario del mouse en el error.

1. Seleccione la ortografía correcta.

El error se ha corregido en el texto del tema.

## Descargar un PDF de temas

Es posible que los usuarios deseen descargar un PDF del tema actual para marcar o compartir con otros.

1. Haga clic en [!UICONTROL **Vista previa**] en la parte superior derecha de la pantalla.

1. Haga clic en el [!UICONTROL **PDF**] sobre el tema. Aparecerá un cuadro de diálogo.

   ![Exportación de PDF](images/lesson-15/pdf-export.png)

1. Rellene la información de **Nombre de transformación** o **Argumentos de línea de comandos DITA-OT** si es necesario. Tenga en cuenta que un PDF sigue generando si todos los campos se dejan en blanco.

1. Haga clic en [!UICONTROL **Descargar**]. El PDF genera.

1. Utilice los iconos disponibles para configurar, descargar o compartir el tema del PDF.

## Buscar un tema en el repositorio o en el mapa

1. Abra el tema.

1. Haga clic con el botón secundario del mouse en la ficha Título.

1. Seleccione **Buscar En**.

1. Elija **Repositorio** o **Mapa** para ir a la ubicación del tema que desee.

## Versión de un tema

1. Realice un cambio en un tema.

1. Guarde el tema.

1. Haga clic en el icono **Repositorio** en el menú superior izquierdo.

   ![Icono de repositorio](images/lesson-15/repository-icon.png)

1. En el cuadro de diálogo, agregue **Comentarios para la nueva versión**.

   ![Cuadro De Diálogo Nueva Versión](images/lesson-15/version-dialog.png)

1. Haga clic en [!UICONTROL **Guardar**].

El número de versión se actualiza.

## Cargar etiquetas de versión

Puede resultar difícil intentar rastrear el estado de un tema basándose únicamente en el número de versión. Las etiquetas facilitan la identificación del estado exacto de un tema que ha sufrido varias revisiones.

1. Seleccione un **perfil de carpeta**.

1. En el Perfil de carpeta, configure el Editor XML.

   a. Seleccione Editar en la parte superior izquierda de la pantalla.

   b. En Etiquetas de versión de contenido XML, agregue un tema nuevo o utilice uno existente.

   ![Etiquetas de versión de contenido](images/lesson-15/version-labels.png)

1. Seleccione [!UICONTROL **Cargar**].

1. Elija un archivo como ReviewLabels.json o similar. Los detalles sobre cómo crear un archivo de este tipo se tratan en otro vídeo.

1. Haga clic en [!UICONTROL **Abrir**].

1. Haga clic en [!UICONTROL **Guardar**] en la parte superior izquierda de la pantalla Perfil de carpeta.

1. Haga clic en [!UICONTROL **Cerrar**] en la parte superior derecha.

Las etiquetas de versión ya están cargadas.

## Asignar etiquetas de versión

1. Cargue las etiquetas de versión.

1. Haga clic en el icono [!UICONTROL **Preferencias de usuario**] en la parte superior izquierda del tema actual.

   ![Perfil de carpeta](images/lesson-15/folder-profile-icon.png)

1. Seleccione el mismo Perfil de carpeta en el que se cargaron las etiquetas de versión anteriormente.

1. En el cuadro de diálogo Preferencias de usuario, asegúrese de que la Ruta base hace referencia a la misma información a la que se ha aplicado el Perfil de carpeta.

   ![Preferencias de usuario](images/lesson-15/user-preferences.png)

1. Haga clic en [!UICONTROL **Guardar**].

1. Versión del tema.

1. Añada un comentario y seleccione una etiqueta de versión en la lista desplegable.

   ![Cuadro De Diálogo Etiqueta De Nueva Versión](images/lesson-15/labels-dialog.png)

1. Haga clic en [!UICONTROL **Guardar**].

El número de versión se actualiza.

## Ver el historial de versiones y etiquetas

1. En el panel izquierdo, busque el título del tema actual.

1. Haga clic en el título para abrir el menú contextual.

1. Seleccione [!UICONTROL **Ver en la IU de Assets**].

   ![IU DE Assets](images/lesson-15/view-assets-ui.png)

   - El historial de versiones con etiquetas se muestra a la izquierda.

   ![Historial de versiones](images/lesson-15/version-history.png)

1. Haga clic en una versión para acceder a opciones como **Revertir a esta versión** y **Vista previa de la versión**.

## Crear una plantilla nueva

Existen plantillas tanto para temas como para mapas. Los administradores pueden acceder a Plantillas en el panel izquierdo.

1. Haga clic en [!UICONTROL **Plantillas**] en el panel izquierdo.

1. Seleccione Mapa o Tema para abrir el menú contextual asociado.

1. Haga clic en para añadir la nueva plantilla.

   ![Plantilla de nuevo tema](images/lesson-15/version-history.png)

1. Rellene los campos en el cuadro de diálogo resultante.

Aparecerá la plantilla de shell, que contiene contenido de muestra y una estructura de muestra.
