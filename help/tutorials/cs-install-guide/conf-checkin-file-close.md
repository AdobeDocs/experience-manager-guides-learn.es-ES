---
title: Configurar la solicitud para proteger un archivo al cerrar
description: Obtenga información sobre cómo configurar el mensaje para proteger un archivo al cerrar
source-git-commit: 4f15166b1b250578f07e223b0260aacf402224be
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# Configurar la solicitud para proteger un archivo al cerrar {#id222HC040PE8}

Cuando el usuario intenta cerrar un archivo que se abre en el Editor Web utilizando **Cerrar** en la pestaña del archivo o en el **Cerrar** opción en el menú Opciones, aparece un cuadro de diálogo si el archivo tiene datos sin guardar o una versión sin guardar. Se solicitará al usuario que desbloquee el archivo si está bloqueado.

Siga las instrucciones que se indican en [Anulaciones de configuración](download-install-additional-config-override.md#) para crear el archivo de configuración. En el archivo de configuración, proporcione los siguientes detalles \(property\) para configurar una solicitud de protección de un archivo al cerrar:

| PID | Clave de propiedad | Valor de propiedad |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.checkin` | Boolean \( true/ false\).<br> **Valor predeterminado**: false |

Cuando esta configuración está habilitada, la variable **Desbloquear el archivo** La casilla de verificación está seleccionada de forma predeterminada en el cuadro de diálogo.

Para obtener más información, consulte *Escenarios de archivo, cerrar y guardar* de la guía as a Cloud Service Uso de guías de Adobe Experience Manager.

**Tema principal:**[ Personalizar editor web](conf-web-editor.md)
