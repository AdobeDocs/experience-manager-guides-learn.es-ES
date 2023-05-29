---
title: Utilice variables para establecer las opciones Ruta de destino, Nombre del sitio o Nombre de archivo
description: Aprenda a utilizar variables para establecer las opciones Ruta de destino, Nombre del sitio o Nombre de archivo
exl-id: e8d5b7c7-4f80-4ab6-9ad1-308bf0d4cf74
source-git-commit: 8073716bccacbe8d6a158b44d5106b083e3a5dcd
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Utilice variables para establecer las opciones Ruta de destino, Nombre del sitio o Nombre de archivo


AEM Al generar resultados en el sitio o en los PDF AEM, puede utilizar variables para definir las opciones Ruta de destino, Nombre del sitio o Nombre de archivo del PDF, según sea el caso. Puede utilizar una sola variable o una combinación de ellas para definir estas opciones.

La siguiente tabla enumera las variables que se admiten de forma predeterminada:

| Variable | Ruta de destino final | Ejemplos |
| --- | --- | --- |
| `${map_filename}` | Utiliza el nombre de fichero de mapa DITA para crear la ruta de destino. | **Nombre de archivo de mapa DITA**:<br>`AEMGuides.ditamap`<br><br>**Ruta de destino** configurado como:<br>`/content/output/sites/${map_filename}`<br><br>**Ubicación de salida final**:<br>`/content/output/sites/aemGuides/AEMGuides.html` |
| `${map_title}` | Utiliza el título del mapa DITA para crear la ruta de destino. | **Nombre de archivo de mapa DITA**:<br>`AEMGuides.ditamap`<br><br>**Título de mapa DITA**:<br>`AEMGuides`<br><br>**Ruta de destino** configurado como:<br>`/content/output/sites/${map_title}`<br><br>**Ubicación de salida final**:<br>`/content/output/sites/AEMGuides/AEMGuides.html` |
| `${preset_name}` | Utiliza el nombre del ajuste preestablecido de salida para crear la ruta de destino. | **Nombre de ajuste preestablecido de salida**:<br>`AEM Guides PDF Output`<br><br>**Nombre de archivo de mapa DITA**:<br>`SampleDita.ditamap`<br><br>**Ruta de destino** configurado como:<br>`/content/output/sites/${preset_name}`<br><br>**Ubicación de salida final**:<br>`/content/output/sites/AEM Guides PDF Output/SampleDita.html` |
| `${language_code}` | Utiliza el código de idioma donde se encuentra el archivo de asignación para crear la ruta de destino. | **Nombre de archivo de mapa DITA**:<br>`SampleDita.ditamap`<br><br>**Ruta del archivo de mapa DITA**:<br>`/content/dam/projects/AEM-Guides/en/user-guide/`<br><br>**Ruta de destino** configurado como:<br>`/content/output/sites/${language_code}`<br><br>**Ubicación de salida final**:<br>`/content/output/sites/en/SampleDita.html` |
| `${map_parentpath}` | Utiliza la ruta completa del archivo de asignación para crear la ruta de destino.<br><br>**Nota** AEM :Esta variable no se puede usar para especificar el Nombre del sitio o el Nombre del archivo del PDF de la. | **Nombre de archivo de mapa DITA**:<br>`SampleDita.ditamap`<br><br>**Ruta del archivo de mapa DITA**:<br>`/content/dam/projects/AEM-Guides/en/user-guide`/<br><br>**Ruta de destino** configurado como:<br>`/content/output/sites/${map_parentpath}`<br><br>**Ubicación de salida final**:<br>`/content/output/sites/content/dam/projects/AEM-Guides/en/user-guide/SampleDita.html` |
| `${path_after_langfolder}` | Utiliza la ruta del archivo de asignación después de la carpeta de idioma para crear la ruta de destino.<br><br>**Nota** AEM : Esta variable no se puede utilizar para especificar el nombre del sitio o el nombre del archivo del PDF de la. | **Nombre de archivo de mapa DITA**:<br>`SampleDita.ditamap`<br><br>**Ruta del archivo de mapa DITA**:<br>`/content/dam/projects/AEM-Guides/en/user-guide/`<br><br>**Ruta de destino** configurado como:<br>`/content/output/sites/${path\_after\_langfolder}`<br><br>**Ubicación de salida final**:<br>`/content/output/sites/user-guide/SampleDita.html` |

Además, también se pueden utilizar los metadatos definidos para el fichero de mapa DITA o de mapa de libros como variables. Los metadatos se encuentran en `/jcr:content/metadata` nodo del mapa DITA o archivo bookmap. Por ejemplo, una de las propiedades de metadatos definidas en la variable `/jcr:content/metadata` el nodo es `dc:title`. Puede especificar `${dc:title}` y el valor del título se utiliza en la salida final.
**Tema principal:**[ Generación de salida](generate-output.md)