---
title: Crear y publicar con líneas base
description: Crear y publicar con líneas de base en  [!DNL Adobe Experience Manager Guides]
exl-id: 3c229c30-f2e0-4fb0-b60c-7bae60ef1a5b
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 2%

---

# Crear y publicar con líneas base

El uso de una línea de base permite crear una versión de los temas del mapa y del contenido de referencia relacionado. Esto puede basarse en una fecha u hora específicas o en etiquetas.

>[!VIDEO](https://video.tv.adobe.com/v/338993?quality=12&learn=on)

## Acceso a la pestaña Líneas base en el panel de mapas

Puede acceder a sus líneas de base en el panel de mapas.

1. Vista de repositorio, seleccione el icono de puntos suspensivos del mapa para abrir el menú Opciones y, a continuación, **Abrir panel de mapa.**

   ![elipsis-map-dashboard.png](images/ellipsis-map-dashboard.png)
El tablero de mapas se abre en otra pestaña.

1. Seleccionar **líneas base**.

   ![baseline-tab.png](images/baseline-tab.png)

Se muestra la pestaña Líneas base.

## Creación de una línea base basada en etiquetas

1. En la pestaña Líneas bases, seleccione **Crear**.

   ![create-baseline.png](images/create-baseline.png)

   Se muestra la información de la nueva línea base. Su nombre predeterminado se basa en la fecha de creación.

1. Asigne un nuevo nombre a la línea de base, si es necesario.

1. Bajo el encabezado &quot;Establecer la versión basada en&quot;, seleccione el círculo para Etiqueta.
   ![set-the-version.png](images/set-the-version.png)

   >[!NOTE]
   >
   >NOTA: La casilla de verificación *Usar la última versión si la etiqueta no está presente* está seleccionada de forma predeterminada. Si no se selecciona y existen temas o archivos multimedia sin la etiqueta elegida en el mapa, el proceso de creación de Línea base fallará.

1. Introduzca la etiqueta que desee utilizar.

1. Seleccione **Guardar**.

Se crea la línea base. Se muestra una tabla de todos los temas y su información asociada.

### Uso de la función Examinar todos los temas

La función Examinar todos los temas permite ver la información del tema, incluida la versión y la etiqueta, así como especificar la versión utilizada. Puede acceder a él seleccionando **Examinar todos los temas** al crear o editar su línea de base.

![browse-all-topics.png](images/browse-all-topics.png)

## Creación de una línea base basada en fecha y hora

También puede crear líneas base que sean una instantánea en el tiempo.

1. Asegúrese de que la pestaña Líneas bases esté abierta y seleccione Crear.

   ![create-baseline.png](images/create-baseline.png)

1. Bajo el encabezado &quot;Establecer la versión basada en&quot;, seleccione el círculo para &quot;Versión activada&quot;.

   ![version-on.png](images/version-on.png)

1. Seleccione el icono de calendario y especifique la fecha y la hora que desee.

   ![calendario.png](images/calendar.png)

1. Asigne un nombre nuevo a la línea base si es necesario.

1. Seleccione **Guardar**.

Se crea la línea base. Se muestra una tabla de todos los temas y su información asociada.

### Adición de etiquetas a la línea base

Es posible que desee asignar una nueva etiqueta de forma masiva a todo el contenido del mapa.

1. Seleccione la línea de base para la que desea añadir etiquetas.

1. Seleccione **Agregar etiquetas**.

   ![add-labels.png](images/add-labels.png)

   Aparece el cuadro de diálogo Agregar etiqueta.

1. Escriba la etiqueta que desee asignar y seleccione **Agregar**.

La etiqueta se ha agregado a todos los temas.

## AEM Generación de una salida del sitio de la mediante una línea de base

1. Vaya a la pestaña Ajustes preestablecidos de salida en el panel de mapas.

1. AEM Seleccione la casilla de verificación Sitio de.

   ![aem-site-checkbox.png](images/aem-site-checkbox.png)

1. Seleccione **Editar**.

   ![edit-aem.png](images/edit-aem.png)

   Aparece una nueva página.

1. Seleccione la casilla de verificación Usar línea de base y elija la línea de base que desee utilizar en el menú desplegable.

   ![baseline.png](images/baseline.png)

1. Seleccione **Listo**.

   ![hecho.png](images/done.png)

1. Seleccione **Generar**.

   ![generate.png](images/generate.png)

   El resultado se ha generado con una línea de base.

## Visualización del resultado generado

1. Vaya a la pestaña Salidas en el panel de mapas.

1. Seleccione el texto de la columna Configuración de generación para abrir la salida.
   ![aem-site-link.png](images/aem-site-link.png)

## Eliminación de una línea base

1. En la pestaña Líneas bases, seleccione la línea base que desee eliminar.

1. Seleccione **Quitar**.

   ![remove-baseline.png](images/remove-baseline.png)

   Aparece el cuadro de diálogo Quitar línea base.

1. Seleccione **Quitar**.

Se elimina la línea de base.

## Duplicación de una línea base

1. En la pestaña Líneas bases, seleccione la línea base que desea duplicar.

1. Seleccione **Duplicado**.

   ![duplicate.png](images/duplicate.png)

1. Seleccione **Guardar**.

   ![save.png](images/save.png)

Se crea la línea base duplicada.

## Modificación de una línea base

Puede especificar directamente la versión de un tema utilizado en una línea de base.

1. En la pestaña Líneas bases, seleccione la línea base que desee modificar.
1. Seleccione **Editar**.

   ![edit-aem.png](images/edit-aem.png)

1. Seleccione **Examinar Todos Los Temas**.

   ![browse-all-topics.png](images/browse-all-topics.png)

   Se muestra una tabla de temas y su información asociada.

1. Para los temas que desee modificar, seleccione la versión que desee en el menú desplegable de la columna Versión.

   ![version-dropdown.png](images/version-dropdown.png)

1. Seleccione **Guardar**.

Se han guardado sus cambios. La línea de base utilizará ahora las versiones del tema que haya especificado.

## AEM Creación de un ajuste preestablecido de salida del sitio personalizado

Es difícil distinguir entre salidas predeterminadas del mismo tipo en la pestaña Output. El uso de un ajuste preestablecido de salida personalizado con un nombre único y fácil de usar le permite solucionar este problema.

En este caso, se crea un ajuste preestablecido de salida basado en una línea de base.

1. Vaya a la pestaña Ajustes preestablecidos de salida en el panel de mapas.

1. Seleccione **Crear**.

   ![create-output-preset.png](images/create-output-preset.png)

   Se muestra una nueva página de ajuste preestablecido de salida, denominada Nueva salida.
1. En el campo Nombre de configuración, introduzca un nombre descriptivo.

1. Seleccione la casilla Usar instantánea (Use Baseline) y seleccione la instantánea que desee en el menú desplegable.

   ![baseline.png](images/baseline.png)

1. Seleccione **Listo**.

Se ha creado el nuevo ajuste preestablecido de salida, que se muestra en la página Ajustes preestablecidos de salida.
