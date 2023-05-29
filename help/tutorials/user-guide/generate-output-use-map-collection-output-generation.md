---
title: Usar la colección de mapas para generar resultados
description: Obtenga información sobre cómo utilizar la colección de mapas para la generación de resultados
exl-id: 32e3af6c-9670-42cc-8dbe-9f99fbc60adf
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 1%

---

# Usar la colección de mapas para generar resultados {#id1723F20G0HS}

En cualquier organización, un producto puede tener varios tipos de documentación. Como especialista en publicación, le gustaría controlar qué salida desea generar para qué documento. Además, debe haber una forma de publicar varios documentos por lotes con un solo clic.

AEM Guías de permite organizar el contenido para publicarlo mediante un panel denominado Colección de mapas. Una colección de mapas permite ensamblar todos los tipos de documentos en una sola unidad. Puede elegir qué tipo de salida desea generar para cada documento de la colección de mapas. Además, también puede generar resultados y ver el progreso de generación de resultados desde el panel de publicación.

La colección de mapas le ofrece la opción de ver si hay algún cambio en algún mapa respecto al último resultado publicado. Puede ver los detalles en la pestaña Mapas y ajustes preestablecidos de su colección de mapas y, a continuación, volver a publicar la salida si es necesario. Para obtener más información, vea Agregar un mapa a una colección de mapas.

## Creación de una colección de mapas y adición de mapas DITA

Para crear una colección de mapas y añadir mapas DITA a la colección, realice los siguientes pasos:

1. En la IU de Assets, haga clic en **Asignar colecciones**.

   Si el vínculo Asignar colecciones no está disponible, seleccione la opción **Navegación** en el carril izquierdo y haga clic en **Asignar colecciones**.

   ![](images/access-map-collection-left-rail.png){width="350" align="left"}

1. Escriba un Título para la colección de mapas.
1. Haga clic en **Crear**.

   Se muestra un mensaje de éxito al crear la colección de mapas.

1. Clic **Cerrar** en el mensaje de éxito.

   El fichero de mapa recién creado se muestra en la página Colecciones de mapas.

1. Haga clic en el cuadro gris del mosaico de la colección que desea editar.
1. Clic **Editar** y luego haga clic en **Agregar asignaciones**.
1. Busque y añada las asignaciones DITA que desee añadir a la colección de asignaciones.

   De forma predeterminada, todos los ajustes preestablecidos y configuraciones regionales asociados con el mapa se añaden automáticamente.

1. Seleccione la salida deseada activando o desactivando el botón deslizante.
1. Haga clic en **Listo**.

   Los ficheros de mapa DITA se añaden a la colección de mapas.

   ![](images/maps_presets_62_63.png){width="800" align="left"}

Las siguientes opciones de filtrado y detalles de asignación se muestran en la página de recopilación:

- **Filtro:** El último carril muestra los siguientes filtros:
   - **Modificado**: puede seleccionar Sí o No. Si selecciona Sí, sólo se mostrarán los mapas DITA modificados en la tabla Mapas y ajustes preestablecidos.
   - **Preestablecido**: seleccione un ajuste preestablecido para el que desee filtrar los archivos de asignación. Por ejemplo, si elige *AEM Sitio web de* preestablecido, solo se muestran las asignaciones que tienen el *AEM Sitio web de* Ajuste preestablecido de salida configurado en ellos.
   - **Idioma**: Puede seleccionar cualquiera de los códigos de idioma disponibles y mostrar solo el idioma seleccionado en la tabla Mapas y ajustes preestablecidos.
- **Mapas y ajustes preestablecidos** tabla: la tabla Mapas y ajustes preestablecidos presenta información en las siguientes columnas:
   - **Mapa**: muestra el título del fichero de mapa DITA.
   - **Idioma**: muestra el idioma del mapa DITA.
   - **Preestablecido**: Muestra el tipo de ajuste preestablecido de salida configurado en el archivo de asignación.
   - **Modificado**: indica si el mapa DITA se actualiza después de la última publicación. En función de esta información, puede decidir si desea volver a publicar la salida para este mapa DITA o no.
   - **Última generación**: Muestra la fecha y la hora de la última salida generada.

## Configure y genere la salida mediante una colección de mapas

Para configurar y generar la salida mediante una colección de mapas, realice los siguientes pasos:

1. Abra la colección Mapa.
1. \(Opcional\) Realice cualquiera de las siguientes acciones según sus necesidades:
   - Aplique filtros desde el carril izquierdo para filtrar los mapas modificados, los ajustes preestablecidos de salida o el idioma.
   - Si es necesario, haga clic en **Editar** y active o desactive el botón deslizante para cambiar la salida deseada.
1. Realice una de las siguientes acciones:

   - Para generar la salida de las asignaciones seleccionadas, seleccione los archivos de asignación y haga clic en **Generar seleccionados**.
   - Para generar la salida de todos los mapas DITA con los ajustes preestablecidos configurados, pulse en **Generar todo**.

   >[!IMPORTANT]
   >
   > Si un proceso de generación de salida para un ajuste preestablecido o un mapa DITA está en cola o en curso, no se puede iniciar otra tarea de generación de salida para el mismo ajuste preestablecido o mapa.


## Eliminar una colección Map o un mapa DITA de la colección Map

- Para eliminar una colección de mapas, seleccione una colección en la página Colección de mapas y haga clic en **Eliminar**.
- Para eliminar un mapa DITA de una colección de mapas, abra la colección de mapas en el modo Edición, seleccione el fichero de mapa DITA y pulse en **Quitar de la colección**.

   De esta forma, también se eliminarán los ajustes preestablecidos o configuraciones regionales asociados al mapa DITA de la recopilación de mapas.


## Cancelar una tarea de generación de resultados de una colección de mapas

Similar a la forma de cancelar una tarea de generación de resultados desde el [Consola de mapa DITA](generate-output-for-a-dita-map.md#id2061H100T5Z) o el [Publicar tablero](generate-output-publish-dashboard.md#), puede cancelar una tarea de generación de resultados desde una colección de mapas. Acceda a la pestaña Resultados de una colección de mapas, vaya a la tarea de publicación que desee cancelar y haga clic en **Cancelar este trabajo** para cancelar la tarea de publicación.

![](images/cancel-publish-task-map-collection.png){width="800" align="left"}

**Tema principal:**[ Generación de salida](generate-output.md)