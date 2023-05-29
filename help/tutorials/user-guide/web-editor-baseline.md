---
title: Crear y administrar líneas de base desde el editor web
description: Obtenga información sobre cómo crear y administrar líneas de base desde el editor web
exl-id: 9e390489-16f5-4f9a-a821-5150a66c2ed4
source-git-commit: 3bca42f0954afc2362ab24f369e698113324dbc3
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 0%

---

# Crear y administrar líneas de base desde el editor web {#id223MB0ZF043}

>[!TIP]
>
> AEM Se recomienda utilizar esta función Línea base del Editor Web si ha actualizado a la versión de marzo as a Cloud Service de Guías de la versión o posterior.

AEM Guías de proporciona la función Línea base integrada dentro del Editor web que permite a los usuarios crear líneas de base y utilizarlas para publicar o traducir temas de diferentes versiones.

## Crear una línea base

Puede crear una línea base desde el Editor Web realizando los siguientes pasos:

1. En el panel Repositorio, abra el fichero de mapa DITA en la vista Mapa.
1. Haga clic en **Administrar** pestaña. El **Línea base** El panel muestra las líneas de base del mapa DITA.

   ![](images/baseline-manage.png){width="800" align="left"}

1. En el **Línea base** , haga clic en el icono + en la parte superior derecha. Puede crear una línea base con una versión específica de los temas y contenido referenciado disponible en una fecha y hora específicas, o con una etiqueta definida para una versión de los temas.
1. Introduzca un nombre para la línea base en **Nombre de línea base**.
1. Entrada **Opción de línea base**, puede elegir entre **Usar versión de archivo** opción o **Uso de etiquetas** opción:

   **Usar versión de archivo**: Puede crear una línea base estática con una versión específica de los temas y contenido referenciado disponible en una fecha y hora específicas, o con una etiqueta definida para una versión de los temas:

   - Entrada **Establezca la última versión basada en,** seleccione una de las siguientes opciones:


      1. **Fecha** &lt;time stamp=&quot;&quot;>: elige la versión de los temas en la fecha y hora especificadas.
      1. **Etiqueta**: seleccione esta opción para elegir los temas según la etiqueta aplicada a ellos. Si los temas tienen etiquetas especificadas, estas se enumeran en la lista desplegable. Puede elegir una etiqueta de la lista. También puede agregar una etiqueta en el cuadro de texto.\
         Al seleccionar **Etiqueta,** puede elegir las referencias directas e indirectas.
      - Para las referencias directas dentro del mapa DITA, se le ofrece la opción de utilizar la última versión de temas que no tienen la etiqueta especificada aplicada.

      >[!NOTE]
      >
      > Si introduce una etiqueta que no existe, seleccione la opción **No crear una línea base** a continuación, la creación de la línea base falla y muestra un mensaje de error cerca del nombre de la línea base en el panel Línea base.

      - Para las referencias indirectas dentro del mapa DITA, se ofrece una opción adicional para utilizar la versión más reciente de temas que no tengan aplicada la etiqueta especificada. También puede elegir **Seleccionar automáticamente** para el contenido referenciado, y el sistema selecciona automáticamente la versión del contenido referenciado correspondiente a la versión del contenido en el que se hace referencia.

   Una vez seleccionada una etiqueta o versión como en la fecha, todos los temas a los que se hace referencia y los archivos multimedia dentro del mapa se seleccionan según corresponda. Esta selección de temas no se muestra en la interfaz de usuario, pero se guarda en el servidor.

   **Usar etiquetas**: seleccione esta opción para la creación de la línea base para seleccionar los temas según la etiqueta aplicada.

   Las líneas bases basadas en etiquetas se actualizan dinámicamente. Si genera una línea de base, descarga una línea de base o crea un proyecto de traducción utilizando una línea de base, los archivos se seleccionan dinámicamente en función de las etiquetas actualizadas. Por ejemplo, si ha utilizado la versión 1.2 de un tema con Label Release 1.0 para la línea de base y ha actualizado la versión 1.5 con Label Release 1.0 más adelante, la línea de base se actualizará dinámicamente y se utilizará la versión 1.5.

   ![](images/dynamic-baseline.png){width="550" align="left"}

   - **Seleccionar etiquetas**: Si los temas tienen etiquetas especificadas, las etiquetas se enumeran en la **Seleccionar etiquetas** desplegable. Puede elegir la etiqueta\(s\) de la lista. Las etiquetas seleccionadas primero reciben una prioridad mayor que las posteriores.
1. **Referencias indirectas**: para referencias indirectas dentro del mapa DITA, se ofrecen las siguientes opciones:

   - **Seleccionar automáticamente**: puede elegir entre **Seleccionar automáticamente** para el contenido referenciado, y el sistema selecciona automáticamente la versión del contenido referenciado correspondiente a la versión del contenido en el que se hace referencia.

   - **Usar etiqueta seleccionada**: puede crear una línea base con la etiqueta seleccionada definida para una versión de los temas.
   - **Utilizar la última versión o la copia de trabajo**: utilice la versión más reciente de los temas a los que no se les haya aplicado la etiqueta especificada o, si no se ha creado ninguna versión, utilice la copia de trabajo de los temas para crear la línea base.
1. Haga clic en **Aplicar**.

Se crea la línea base. La creación de la línea de base se produce de forma asíncrona, por lo que puede seguir trabajando en otros archivos en el Editor Web. Una vez creada la línea base, aparece un mensaje emergente que confirma que se ha creado la línea base y también recibe una notificación en la bandeja de entrada para el mismo.

## Administrar líneas base

Puede gestionar las líneas base existentes mediante las distintas funciones del tablero de mandos Línea base.

- Puede buscar una línea base existente mediante el cuadro de texto del panel Línea base. Utilice el **Aplicar filtro** para mostrar todas las líneas base o enumerarlas con el estado de creación Correcto, En curso o Fallido.
- Utilice el **Actualizar** en el panel Línea base para volver a comprobar todas las líneas base y mostrar una nueva lista de líneas base para el mapa DITA abierto en la vista Mapa.
- Para ver o editar el contenido de una línea base existente, pulse dos veces en la línea base de la lista del panel Línea base. La ventana de edición de línea base del centro muestra el fichero de mapa DITA, el contenido o los temas del mapa y el contenido referenciado.


![](images/baseline-options.png){width="550" align="left"}

También se pueden realizar las siguientes operaciones en la instantánea desde el menú Opciones (Options):

- **Editar**, **Duplicado,** o **Eliminar** una línea base existente.
- Añada, quite o realice cambios en etiquetas existentes desde el **Administrar etiquetas** opción. Si el administrador ha configurado etiquetas predefinidas, dichas etiquetas se muestran en la lista desplegable Añadir etiqueta. Para obtener más información sobre cómo añadir etiquetas, consulte [Uso de etiquetas](web-editor-use-label.md#).

   >[!NOTE]
   >
   > El proceso para agregar o quitar etiquetas se produce de forma asíncrona, por lo que puede seguir trabajando en otros archivos en el Editor Web. Una vez añadida o eliminada la etiqueta, se muestra un mensaje emergente que confirma que la etiqueta se ha añadido o eliminado, y también recibe una notificación en la bandeja de entrada para el mismo.

- **Editar propiedades** de una línea base existente que haya definido al crear la línea base.
- Exportar la instantánea de una instantánea en un archivo CSV con el **Exportar línea base** opción.

**Filtros de línea base**

Uso del icono Filtros en la **Filtros de línea base** panel puede aplicar filtros en la línea de base abierta en la ventana de edición de la línea de base:

![](images/baseline-filter.png){width="350" align="left"}

- Filtre los archivos en función de sus nombres o ubicación.
- Filtre los archivos en función de los valores de diferentes columnas, como Tipo de archivo, Tipo de referencia, etc.
- Seleccione las columnas que desea mostrar en la ventana de edición de la instantánea.

>[!NOTE]
>
> Puede hacer clic en un encabezado de columna y ordenar los archivos en función de las columnas de la ventana de edición de línea de base.

**Guardar o restablecer una línea base**

Una vez editada la línea base, puede hacer clic en **Guardar** en la parte superior para guardar los cambios realizados en la línea base. Puede hacer clic en **Restablecer** botón si no desea guardar el cambio y restablecer la línea de base. Al hacer clic en **Restablecer** botón se muestra una advertencia que indica que se perderán los cambios no guardados.

**Tema principal:**[ Trabajar con el editor web](web-editor.md)