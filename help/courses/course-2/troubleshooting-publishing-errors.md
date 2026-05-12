---
title: Solución de problemas de publicación
description: Solucionar problemas de publicación en  [!DNL Adobe Experience Manager Guides]
exl-id: b37ea3e7-59cf-4fc5-8fae-e1fadd26f8d8
TQID: https://experienceleague.adobe.com/xUPH5-Fh7uZDO6jaITHCsZfUmVuNtNrxoiAxSRkHvBo
product_v2: id: fae5e35a-80c9-4b94-9352-1a060a6aab1did: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a3bd6397-2eb2-4908-a61c-226e26855dca
subfeature_v2: id: fd6cc9e1-e5e5-494e-b7b1-a32f2d6cd7c9
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 27ffc636d63300fb2e99903d92cab12f0cfcbb25
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 0%

---

# Solución de problemas de publicación

La publicación de un mapa suele ser sencilla. Abra el mapa, seleccione un ajuste preestablecido de salida y genere la salida. Sin embargo, si un mapa o sus temas contienen errores, la generación de resultados puede fallar. Cuando esto sucede, es importante saber cómo solucionar problemas.

>[!VIDEO](https://video.tv.adobe.com/v/338990?quality=12&learn=on)

## Preparación para el ejercicio

Puede descargar archivos de ejemplo para el ejercicio aquí.

[Descarga de ejercicio](assets/exercises/publishing-basic-to-advanced.zip)

## Causas comunes de errores de publicación

Los errores pueden introducirse en el contenido de origen. Por ejemplo:

* Referencia de ruta de archivo con nombre incorrecto

* Carpeta con nombre incorrecto

* Falta el gráfico o el archivo

* Referencia de contenido configurada incorrectamente

* Referencia cruzada rota

* Errores en los valores de un atributo (por ejemplo, una cadena en lugar de un número)

* Configuración incorrecta de los componentes utilizados por [!DNL AEM Guides]

## Impacto de los errores

Un error puede ser menor y dar como resultado una nota simple para hacerle saber que un archivo no se empaquetó correctamente o lo suficientemente grave como para que resulte en un error completo al generar resultados. La pestaña Salidas muestra iconos con códigos de color para mostrar el éxito, los errores o los errores relacionados con la generación de salidas.

![impacto de error](images/error-impact.png)

## Abrir y revisar registros de errores

El archivo de registro generado se puede abrir para su revisión.

1. En la ficha **Salidas**, haga clic en la fecha y hora bajo Generado a las.****

   ![registro de errores](images/error-log.png)

1. Desplácese por el registro de errores.

## Mostrar y ocultar tipos de error

El registro de errores muestra cada tipo de error en un color único.

![navegar-errores](images/navigate-errors.png)

1. **Seleccione** o **anule la selección** de cualquier tipo de error para mostrar u ocultar el resaltado.

1. Navegar por errores utilizando los botones **next** o **previous** (flechas).

## Resolución de errores

Según el tipo de error, la resolución puede ser simple o compleja. Puede ser completado por un autor en el Editor XML o puede requerir que un administrador trabaje con [!DNL AEM Guides]. Las correcciones específicas dependen del error, del impacto y de los flujos de trabajo de la organización.

* Referencia de ruta de archivo con nombre incorrecto

  Los autores pueden actualizar la referencia de ruta en el documento de origen.

* Carpeta con nombre incorrecto

  Los autores pueden actualizar el nombre de la carpeta o mover archivos según sea necesario.

* Falta el gráfico o el archivo

  Los autores pueden cargar un gráfico o archivo que falte, cambiar el nombre de un gráfico o archivo o mover un gráfico o archivo

* Referencia de contenido configurada incorrectamente

  Los autores pueden corregir la ubicación del contenido al que se hace referencia o cambiar la ruta a la referencia de contenido.

* Referencia cruzada rota

  Los autores pueden corregir la ubicación a la que apunta la referencia cruzada o cambiar el nombre o las propiedades del archivo de destino

* Errores en los valores de un atributo (por ejemplo, una cadena en lugar de un número)

  Los autores pueden actualizar el atributo a un valor correcto o los administradores pueden actualizar el sistema para que admita nuevos valores.

* Configuración incorrecta de los componentes utilizados por [!DNL AEM Guides]

  Los administradores pueden actualizar la instalación del sistema, sus componentes o los permisos.
