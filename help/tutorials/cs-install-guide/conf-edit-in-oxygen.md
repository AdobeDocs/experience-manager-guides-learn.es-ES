---
title: Configurar la opción de edición en Oxígeno
description: Aprenda a configurar la opción de edición en el complemento Conector de oxígeno.
source-git-commit: a209e46e41055348402292e20c229890cd0c01cf
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# Configurar la opción de edición en Oxígeno

AEM Guías de también permite a los usuarios editar sus temas DITA y mapas DITA en el complemento Conector de oxígeno.

Siga las instrucciones que se indican en [Anulaciones de configuración](download-install-additional-config-override.md#) para crear el archivo de configuración. En el archivo de configuración, proporcione los siguientes detalles (propiedad) para configurar el **Editar en oxígeno** opción:



| PID | Clave de propiedad | Valor de propiedad |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.editinoxygen` | Boolean \(true/false\). **Valor predeterminado**: false |

>[!NOTE]
>
> Esta configuración está deshabilitada de forma predeterminada y la opción no está disponible en el Editor web.

**Tema principal:**[ Personalizar editor web](conf-web-editor.md)
