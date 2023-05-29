---
title: AEM Configure nombres de archivo válidos para la salida del sitio de la
description: AEM Obtenga información sobre cómo configurar nombres de archivo válidos para la salida del sitio de la
source-git-commit: 801c306fa120e7889d4b9428fd5bee2849bf1956
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# AEM Configure nombres de archivo válidos para la salida del sitio de la {#id214GK0X0KXA}

AEM De forma similar a la lista de caracteres de nombre de archivo válidos permitidos para los temas DITA, también se puede configurar una lista de caracteres de nombre de archivo válidos para la salida de sitio de la publicación de datos de página (). Algunos de los caracteres conocidos que no están permitidos en una dirección URL son: ```'<>`@$```. AEM Estos caracteres se configuran para que se conviertan automáticamente en un guion bajo &quot;_&quot; cuando se encuentren al generar nombres de archivo de salida del sitio de la página de salida del sitio de la página de salida de la página de la página. AEM La configuración que le permite establecer caracteres válidos en la salida de sitio de la lista de caracteres de la lista de distribución de datos está presente en la lista de caracteres de la lista de parámetros de la lista de distribución de datos de `com.adobe.fmdita.common.SanitizeNodeNameImpl` paquete. **Definir el conjunto de caracteres no permitidos para la publicación en AEM Sites** AEM para incluir caracteres que desee reemplazar con un guion bajo en los nombres de archivo de salida del sitio de la lista de caracteres de la lista de caracteres que se van a incluir en la lista de nombres de archivo de salida del sitio.

**Tema principal:**[ Configurar nombres de archivo](conf-file-names.md)
