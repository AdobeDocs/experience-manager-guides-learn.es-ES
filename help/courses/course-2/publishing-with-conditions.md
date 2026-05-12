---
title: Publicación con condiciones
description: Publicación con condiciones con Adobe Experience Manager Guides
exl-id: ea94824a-884b-447f-9562-e6c629b8133b
TQID: https://experienceleague.adobe.com/Ez-rAJNfPH-Dd2lTd65B1bct4lkhoB2Gi6IKc8-A8gI
product_v2:
  - id: fae5e35a-80c9-4b94-9352-1a060a6aab1d
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a3bd6397-2eb2-4908-a61c-226e26855dca
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 27ffc636d63300fb2e99903d92cab12f0cfcbb25
workflow-type: tm+mt
source-wordcount: 371
ht-degree: 4%

---

# Publicación con condiciones

La publicación condicional permite escribir una fuente de contenido para una o varias audiencias, productos o plataformas. A continuación, esta información se puede publicar dinámicamente y solo el contenido requerido específicamente incluido en la salida.

>[!VIDEO](https://video.tv.adobe.com/v/339041?quality=12&learn=on)

## Preparación para el ejercicio

Puede descargar archivos de ejemplo para el ejercicio aquí.

[Descarga de ejercicio](assets/exercises/publishing-with-conditions.zip)

## Marcado de contenido con atributos condicionales

1. Abra el tema que desee modificar.

1. Introduzca el texto que se convertirá en condicional. Por ejemplo, uno o más párrafos, una tabla completa, una figura u otro contenido.

   ![Información de presentación](images/presenting-info.png)

1. Seleccione el contenido específico al que desea asignar un atributo condicional. Por ejemplo, un solo párrafo dentro del origen.

   ![Opción de plantilla](images/template-choice.png)

1. En el carril derecho, asegúrese de que se muestra Propiedades.

1. Añada un atributo para audiencia, producto o plataforma.

1. Asigne un valor al atributo. Se han aplicado las actualizaciones de visualización de contenido para mostrar el marcado condicional.

   ![Especificar-Plantilla](images/specify-template.png)

## Vista previa del contenido condicional

1. Haga clic en **Vista previa**.

1. En **Filtros**, seleccione o anule la selección de las condiciones para mostrar u ocultar.

1. Seleccione o anule la selección de **Resaltar texto de condiciones**.

   ![Contenido-Condicional-De-Vista Previa](images/preview-conditional-content.png)

## Creación de un ajuste preestablecido de condición

Un ajuste preestablecido de condición es una colección de propiedades que definen lo que se va a incluir, excluir o marcar de otro modo durante la generación de resultados.

1. En el tablero de mapas, seleccione la pestaña **Ajustes preestablecidos de condición**.

1. Haga clic en **Crear**.

1. Seleccione **Agregar** (o **Agregar todo**).

1. Asigne un nombre a la condición.

1. Seleccione una combinación de atributo, etiqueta y acción.

   ![Crear-Condición-Ajuste-Preestablecido](images/create-condition-preset.png)

1. Repita el proceso tantas veces como sea necesario.

1. Haga clic en **Guardar**.

## Generación de resultados condicionales

Una vez aplicadas las condiciones al contenido, se puede generar como salida. Puede utilizar un ajuste preestablecido de condición o un archivo DITAval.

## Generación de resultados condicionales mediante un ajuste preestablecido de condición

1. Seleccione la ficha **Ajustes preestablecidos de salida**.

1. Seleccione un ajuste preestablecido de salida.

1. Haga clic en **Editar**.

1. En **Aplicar condición con**, seleccione un ajuste preestablecido de condición.

   ![Generar-salida-condicional](images/generate-conditional-output.png)

1. Haga clic en **Listo**.

1. Genere el ajuste preestablecido de salida y revise el contenido.

## Generación de resultados condicionales mediante un fichero DITAval

El fichero DITAval puede utilizarse para publicar contenido condicional. Esto requiere que se cree o cargue un archivo y, a continuación, se haga referencia a él en la publicación.

1. Seleccione la ficha **Ajustes preestablecidos de salida**.

1. Seleccione un ajuste preestablecido de salida.

1. Haga clic en **Editar**.

1. En Aplicar condición usando seleccione un fichero DITAval.

   ![Generate-Using-DITAval](images/generate-using-ditaval.png)

1. Haga clic en **Listo**.

1. Genere el ajuste preestablecido de salida y revise el contenido.
