---
title: Corrección ortográfica y buscar/reemplazar
description: Uso de la revisión ortográfica y buscar/reemplazar en AEM Guides
exl-id: 5f39618d-a919-4d3c-a4de-2896f2d1bf20
TQID: https://experienceleague.adobe.com/cSdhulSc30KrwsGh1ldB2yn-8eSLccHBpyD-0S1x1M0
product_v2:
  - id: fae5e35a-80c9-4b94-9352-1a060a6aab1d
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 27ffc636d63300fb2e99903d92cab12f0cfcbb25
workflow-type: tm+mt
source-wordcount: 443
ht-degree: 1%

---

# Corrección ortográfica y Buscar/reemplazar

El editor de AEM Guides tiene potentes funciones de revisión ortográfica y de búsqueda y reemplazo.

>[!VIDEO](https://video.tv.adobe.com/v/342768?quality=12&learn=on)

Corregir un error ortográfico

1. Busque un error en un tema abierto, que se muestra con un subrayado rojo.

1. Mantenga pulsado Ctrl + clic en el botón secundario del ratón dentro de la palabra.

1. Elija la ortografía correcta entre las sugerencias.

Si no se sugiere la ortografía correcta, siempre puede editar la palabra manualmente.

## Cambiar a revisión ortográfica de AEM

Es posible que desee utilizar una herramienta de revisión ortográfica que no sea el diccionario predeterminado del explorador.

1. Vaya a **Configuración del editor**.

1. Seleccione la ficha de configuración **General**.

   ![Configuración de revisión ortográfica](images/lesson-11/configure-dictionary.png)

1. Hay dos opciones:

   - **Revisión ortográfica del explorador**: la configuración predeterminada en la que la revisión ortográfica utiliza el diccionario integrado del explorador.

   - **Corrección ortográfica de AEM**: utilícela para crear una lista de palabras personalizada con el diccionario personalizado de AEM.

1. Elija **Corrección ortográfica de AEM**.

1. Haga clic en [!UICONTROL **Guardar**].

Configurar un diccionario personalizado

El administrador puede cambiar la configuración para que el diccionario de AEM reconozca palabras personalizadas como nombres de empresas.

1. Vaya al panel **Herramientas**.

1. Inicie sesión en **CRXDE Lite**.

   ![Icono CRXDE Lite de IU de AEM](images/lesson-11/crxde-lite.png)

1. Vaya al nodo **_/apps/fmdita/config_**.

   ![Nodo de configuración de CRXDE Lite](images/lesson-11/config-node.png)

1. Cree un nuevo archivo.

   a. Haga clic con el botón derecho en la carpeta de configuración.

   b. Elija **Crear > Crear archivo**.

   ![Creación de nuevo archivo de diccionario](images/lesson-11/new-dictionary-file.png)

   c. Asigne un nombre al archivo _&#x200B;**user_dictionary.txt**&#x200B;_.

   ![Texto del diccionario de usuario](images/lesson-11/user-dictionary.png)

   d. Haga clic en [!UICONTROL **OK**].

1. Abra el archivo.

1. Agregue una lista de palabras que desee incluir en el diccionario personalizado.

1. Haga clic en [!UICONTROL **Guardar todo**].

1. Cierre el archivo.

Es posible que los autores tengan que reiniciar su sesión del Editor Web para obtener la lista de palabras personalizada actualizada en el Diccionario AEM.

## Buscar y reemplazar en un solo archivo

1. Haga clic en el icono Buscar y reemplazar de la barra de herramientas superior.

   ![Buscar icono de reemplazo](images/lesson-11/find-replace-icon.png)

1. En la barra de herramientas inferior, escriba una palabra o frase.

1. Haga clic en [!UICONTROL **Buscar**].

1. Si es necesario, escriba una palabra para reemplazar la palabra encontrada.

1. Haga clic en [!UICONTROL **Reemplazar**].

## Buscar y reemplazar en todo el repositorio

1. Vaya a **Repositorio**.

1. Haz clic en el icono [!UICONTROL **Buscar y reemplazar**] en la parte inferior izquierda de la pantalla.

1. Haga clic en el icono [!UICONTROL **Mostrar configuración**].

1. Elija una de estas opciones

   - **Desproteger archivo antes de reemplazar**: si lo habilita un administrador, el archivo se desprotegerá automáticamente antes de reemplazar los términos de búsqueda.

   - **Sólo palabra completa**: restringe la búsqueda para que devuelva únicamente la palabra o frase exacta introducida.

   ![Buscar reemplazo en el repositorio](images/lesson-11/repository-find-replace.png)

1. Haga clic en el icono [!UICONTROL **Aplicar filtro**] para seleccionar la ruta de acceso del repositorio en la que desea realizar la búsqueda.

1. Introduzca los términos que desea buscar y reemplazar.

1. Si es necesario, seleccione **Crear nueva versión después de reemplazar**.

1. Haga clic en [!UICONTROL **Buscar**].

1. Abra el archivo deseado y utilice las flechas para desplazarse de un resultado encontrado al siguiente.

   ![Buscar IU de navegación de reemplazo](images/lesson-11/find-replace-navigation.png)
