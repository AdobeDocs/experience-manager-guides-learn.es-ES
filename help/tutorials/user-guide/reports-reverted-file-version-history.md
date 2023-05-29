---
title: Informe de historial de versiones de archivos revertidos
description: Obtenga información sobre cómo revertir el informe de historial de versiones de archivos
exl-id: fa90b373-742a-4102-b00f-07e4113fef98
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# Informe de historial de versiones de archivos revertidos {#id205BBC00PRK}

Cuando se trabaja en varias versiones simultáneas junto con varios autores, el contenido está destinado a tener varias versiones. Podría haber información común en varias versiones que distintos autores podrían utilizar en su proyecto. Para gestionar estas asignaciones de trabajo, los autores podrían terminar con varias versiones de los archivos. Estas versiones podrían ser simplemente una versión más reciente de un archivo o una versión anterior. Identificar cuándo se revirtió un archivo y por qué es una tarea compleja.

AEM Guías de la versión le permite generar un informe del historial de versiones para un archivo individual o para todos los archivos de una carpeta. Este historial de versiones le proporciona una vista consolidada de todas las versiones de un archivo que se revirtieron y quién creó esas versiones y el motivo para crearlas.

Puede acceder a este informe desde los siguientes lugares:

- **IU de Assets**: seleccionando un archivo y abriendo **Historial de versiones** desde el carril izquierdo. El **Historial de versiones** La vista contiene el **Revertir registros de versión** en la parte inferior del panel. Al hacer clic en este vínculo, se muestra el historial de versiones revertidas del archivo seleccionado.

   ![](images/revert-log-from-assets-ui.png){width="300" align="left"}

- **Previsualización del tema**: cuando obtiene una vista previa de un tema, también puede mostrar el **Historial de versiones** panel desde el carril izquierdo. Aparecerá un panel similar a la interfaz de usuario de Assets desde donde puede hacer clic en **Revertir registros de versión** para acceder al historial de versiones revertidas del documento activo.

- **AEM sección Herramientas** AEM : también puede acceder a este informe desde sección Herramientas. AEM En el siguiente procedimiento se explica cómo acceder al historial de versiones de reversión desde la sección Herramientas de.


Siga estos pasos para acceder al informe Revertir historial:

1. Haga clic en el vínculo Adobe Experience Manager en la parte superior y elija **Herramientas**.

1. Seleccionar **Guías** de la lista de herramientas.

1. Haga clic en **Historial de reversión de versión** mosaico.

   Se muestra una página Revertir historial de versiones en blanco en la que debe buscar y seleccionar un archivo o carpeta para generar el informe.

1. Clic **Mostrar registros** para generar el informe del archivo o la carpeta seleccionados.

   ![](images/revert-version-history-report.png){width="800" align="left"}

   El informe contiene los siguientes detalles:

   - **Nombre de archivo**: título del tema. Al hacer clic en el vínculo del título del tema, se abre la vista previa del tema.

   - **Marca de tiempo**: la fecha y hora en que se revirtió el tema a una versión anterior.

   - **Usuario**: Nombre del usuario que volvió a una versión anterior.

   - **Revertir desde**: El número de versión original del archivo desde el que se revirtió.

   - **Volver a**: Versión a la que se revirtió el archivo.

   - **Comentario**: Cualquier comentario dado por el usuario que revirtió el archivo.


**Tema principal:**[ Informes](reports-intro.md)