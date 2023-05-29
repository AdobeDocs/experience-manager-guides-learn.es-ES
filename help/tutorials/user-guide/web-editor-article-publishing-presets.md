---
title: Cree ajustes preestablecidos de salida desde el editor web
description: Obtenga información sobre cómo crear ajustes preestablecidos de salida desde el editor web
exl-id: 7fde0057-06a5-428e-a91b-9e9386a56270
source-git-commit: 3bca42f0954afc2362ab24f369e698113324dbc3
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Cree ajustes preestablecidos de salida desde el editor web {#id218CL400JW3}

Realice los siguientes pasos para crear ajustes preestablecidos de salida para el mapa DITA:

1. En la interfaz de usuario de Assets, vaya al archivo de asignación que desee editar.

1. Para obtener un bloqueo exclusivo en el archivo de asignación, seleccione el archivo de asignación y haga clic en **Desproteger**.

1. Seleccione el **Editar temas** del menú de acción del archivo de asignación.

   El archivo de asignación se abre para editarlo en el Editor Web.

   >[!NOTE]
   >
   > Puede añadir o eliminar cualquier tema del mapa mediante el Editor de mapas avanzado. Para obtener más información, consulte [Trabajo con el Editor de mapas avanzado](map-editor-advanced-map-editor.md#).

1. En el **Output** , seleccione el icono + para crear un ajuste preestablecido de salida para el mapa DITA.

   ![](images/output-tab-preset_cs.png){width="350" align="left"}

1. Introduzca el nombre del ajuste preestablecido en el cuadro de diálogo Agregar ajuste preestablecido y haga clic en **Añadir**.

1. Introduzca los siguientes detalles de configuración.

   1. Seleccione las opciones necesarias en la **General** pestaña. Puede elegir crear un ajuste preestablecido de salida con o sin condiciones. También puede utilizar un archivo DITVAL. AEM Guías también le permite seleccionar una línea de base para publicar una versión específica del mapa DITA.
   1. AEM Introduzca los detalles del sitio en la sección **AEM** pestaña. **Sitio** muestra la lista de AEM Sites AEM disponibles en el repositorio de la. **Categoría**, **Plantilla de sección**, y **Plantilla de artículo** son los componentes estructurales utilizados para organizar el aspecto de su salida. AEM Están predefinidas en la plantilla del sitio de la.

      >[!NOTE]
      >
      > Actualice cada lista desplegable para obtener la clasificación adicional en la siguiente lista desplegable.

   1. Desde el **Artículos** , seleccione los temas para los que desea generar la salida.
1. Seleccione el **Generar ajuste preestablecido** en la parte superior para generar la salida.

   ![](images/add-preset-articles-tab_cs.png){width="800" align="left"}

1. Verá el estado del proceso de generación de resultados. El **Temas** enumera los temas para los que se genera una salida mientras la variable **Estado** La columna muestra el estado de publicación de cada tema.

   Para ver el resultado, pase el puntero del mouse (ratón) sobre el tema y haga clic en Ver resultados.

   ![](images/add-preset-output-generated_cs.png){width="800" align="left"}


>[!NOTE]
>
> También puede Editar, Cambiar nombre, Duplicar o Eliminar un ajuste preestablecido de salida existente desde el menú Opciones.

![](images/edit-preset_cs.png){width="550" align="left"}

**Tema principal:**[ Publicación basada en artículos desde el editor web](web-editor-article-publishing.md)