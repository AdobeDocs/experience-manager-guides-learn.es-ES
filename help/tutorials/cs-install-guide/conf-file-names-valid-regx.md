---
title: Configure Regx para caracteres de nombre de archivo válidos
description: Obtenga información sobre cómo configurar Regx para caracteres de nombre de archivo válidos
source-git-commit: 4f15166b1b250578f07e223b0260aacf402224be
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---


# Configure Regx para caracteres de nombre de archivo válidos {#id214BD0550E8}

AEM A partir de la versión 3.8 de las Guías de usuario, como administrador, puede definir una lista de caracteres especiales válidos permitidos en los nombres de archivo. En versiones anteriores, los usuarios podían definir nombres de archivo que contenían caracteres especiales como `@`, `$`, `>`, y más. Estos caracteres especiales provocaban problemas al abrir temas desde el panel de mapas DITA o al hacer clic en el vínculo del tema en el índice, lo que a menudo provocaba que la página no se abriera debido a caracteres especiales en la dirección URL.

Si utiliza la configuración que le permite definir una regx para los caracteres de nombre de archivo válidos, tendrá control total sobre cómo se asignan los nombres de archivo internamente en el sistema. Puede definir una lista de caracteres especiales permitidos en los nombres de archivo. De forma predeterminada, la configuración de nombre de archivo válida contiene &quot;`a-z A-Z 0-9 - _`&quot;. Al crear un nuevo archivo, puede tener cualquier carácter especial en el título del archivo, pero internamente se reemplazará con &quot;`-`&quot; en el nombre del archivo. Por ejemplo, puede tener el título del archivo como &quot;Introducción 1&quot; o &quot;Introduction@1&quot;, el nombre de archivo correspondiente generado para ambos casos sería &quot;Introducción-1&quot;.

Cuando defina una lista de caracteres válidos, recuerde que estos caracteres &quot;`*/:[\]|#%{}?&<>"/+`&quot; se reemplazará siempre por &quot;`-`&quot;.

Si no configura la lista de caracteres especiales válidos, el proceso de creación de archivos podría dar algunos resultados inesperados. Para evitar estos errores, se recomienda encarecidamente realizar este cambio de configuración.

Siga las instrucciones que se indican en [Anulaciones de configuración](download-install-additional-config-override.md#) para crear el archivo de configuración. En el archivo de configuración, proporcione los siguientes detalles \(property\) para configurar la regex para los caracteres de nombre de archivo válidos:

| PID | Clave de propiedad | Valor de propiedad |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `valid.characters` | El valor es un patrón regex. Debe tener tres caracteres básicos y la lista debe comenzar con un guión \(-\).<br> **Valor predeterminado**: \[-a-zA-Z0-9\_\] |

>[!NOTE]
>
> AEM De forma similar a la lista de caracteres de nombre de archivo válidos, también puede especificar una lista de caracteres de nombre de archivo válidos para la salida de sitio de la lista de nombres de archivo de salida de la página de datos de sitio de. Para obtener más información, consulte [AEM Configure nombres de archivo válidos para la salida del sitio de la](conf-file-names-valid-regx-aem-site-output.md#).

**Tema principal:**[ Configurar nombres de archivo](conf-file-names.md)
