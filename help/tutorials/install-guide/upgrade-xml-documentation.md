---
title: Actualizar guías de Adobe Experience Manager
description: Obtenga información sobre cómo actualizar las guías de Adobe Experience Manager
source-git-commit: 629a3714e7b75af609238a506688da2674bf31cc
workflow-type: tm+mt
source-wordcount: '2750'
ht-degree: 1%

---


# Actualizar guías de Adobe Experience Manager {#id224MBE0M0XA}

>[!NOTE]
>
> Siga las instrucciones de actualización específicas de la versión con licencia del producto.

AEM Puede actualizar la versión actual de las guías de la aplicación a la versión 4.2.1. de la versión 2008 de la versión 2008 de la Guía de la aplicación de la versión 2010.
- Si utiliza las versiones 4.1, 4.1.x o 4.2, puede actualizar directamente a la versión 4.2.1.
- Si está utilizando la versión 4.0, debe actualizar a la versión 4.2 antes de actualizar a la versión 4.2.1.
- Si utiliza la versión 3.8.5, debe actualizar a la versión 4.0 antes de actualizar a la versión 4.2.
- AEM Si su versión es anterior a la 3.8.5, consulte la sección Guías de actualización de la versión en la guía de instalación específica del producto de.

>[!NOTE]
>
> AEM AEM Debe instalar el paquete de servicio de antes de actualizar la versión de las guías de usuario.

Para obtener más información, consulte los siguientes procedimientos:

- [Actualización de 3.8.5 a la versión 4.0](#id2256DK003E1)
- [Actualización a la versión 4.2](#id22A3F500SXA)
- [Actualización a la versión 4.2.1](#upgrade-version-4-2-1)


>[!IMPORTANT]
>
> Antes de comenzar la actualización, realice una copia de seguridad completa del sistema para evitar la pérdida de datos.

## Actualice de la versión 3.8.5 a la versión 4.0 {#id2256DK003E1}

AEM AEM Si utiliza la versión 3.8.5 de las Guías de la comunidad de usuarios de la versión 3.8.5, puede actualizar a la versión 4.0 de las Guías de la comunidad de usuarios de la versión 3.8.5 de las Guías de la comunidad de usuarios de la comunidad de usuarios de la red de. AEM Con la función de actualización, no es necesario desinstalar la versión anterior de las guías de.

Antes de ejecutar el proceso, hay ciertas tareas que debe completar. Las siguientes subsecciones le guiarán por los requisitos previos, la generación de informes y el proceso de migración. AEM Además, después de instalar las guías de la versión 4.0 de las Guías de los usuarios, puede personalizar varias configuraciones en función de la configuración del cliente.

>[!NOTE]
>
> Este proceso de actualización solo es aplicable de la versión 3.8.5 a la versión 4.0. Para ver el proceso de actualización de la versión 3.4 o superior a la 3.8.5, consulte la *AEM Guías de actualización* de la guía de instalación específica del producto, disponible en la [Página de archivado de ayuda](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).

****Requisitos previos****

AEM Antes de iniciar el proceso de actualización de las Guías de, asegúrese de lo siguiente:

1. Se han importado los comentarios de revisión en los temas abiertos para su revisión.
1. Se cerraron todas las revisiones activas.
1. Se cerraron todas las tareas de traducción.
1. AEM AEM Desinstale las correcciones rápidas de las Guías de instaladas en la parte superior de la versión anterior \(versión principal o de parche\) de las Guías de las Guías de las Guías de las Guías.

**Antes de instalar la versión 4.0**

Antes de instalar la versión 4.0, realice los siguientes pasos:

1. AEM Asegúrese de que, en este punto, Guías de esté en la versión 3.8.5.
1. Descargue el paquete del script de actualización. Para ello, busque &quot;Paquete de actualización de la solución XML Documentation 4.0&quot; en [Portal de distribución de software de Adobe](https://experience.adobe.com/#/downloads/content/software-distribution/es/aem.html) que descargará un archivo zip.
1. AEM Cargue este paquete en mediante el Administrador de paquetes e instálelo.
1. Una vez instalado el paquete de actualización, ejecute los siguientes scripts en el mismo orden y siga las instrucciones dadas:

**Comprobar API de compatibilidad de actualización**

Esta API está diseñada para evaluar el estado actual del sistema e informar si la actualización es posible o no. Para ejecutar este script, almacene en déclencheur el siguiente extremo dado:

|Punto final|/bin/dxml/upgrade/3xto4x/report| |Tipo de solicitud|**GET** AEM Puede utilizar un explorador web en el que haya iniciado sesión en la instancia de la como administrador.| |Respuesta esperada|- En caso de que se puedan mover todos los nodos requeridos, recibirá una comprobación superada. <br>: Si un nodo está presente en la ubicación de destino, se obtiene un error relevante. Limpie el repositorio \(elimine el nodo /var/xml\), vuelva a instalar el paquete de actualización y, a continuación, almacene en déclencheur este extremo de nuevo. <br>**Nota:** AEM Este no es un error común, ya que la ubicación de destino no se usa anteriormente en las guías de la versión 3.. <br> : si este script no se ejecuta correctamente, no continúe y genere un informe para el equipo de éxito del cliente.|

**API de migración de datos del sistema**

Esta API está diseñada para migrar los datos del sistema como se menciona en la [Asignación de migración](#id2244LE040XA) sección.

1. No ejecute este script si la API Comprobar compatibilidad de actualización falla \(no continuar\).
1. Una vez que la API de comprobación de compatibilidad de actualización devuelva un resultado correcto, puede ejecutar el script de actualización.

|Punto final|/bin/dxml/upgrade/3xto4x| |Tipo de solicitud|**POST** Esta secuencia de comandos es una solicitud de POST, por lo que debe ejecutarse a través de agentes como Postman.| |Respuesta esperada|- Una vez completada la migración, puede instalar la solución de XML Documentation versión 4.0.<br>- En caso de errores, restaure al último punto de comprobación y comparta los registros de errores junto con la salida de la API con el equipo de éxito del cliente.|

**Asignación de migración**: la API anterior migra todos los datos de la ubicación de origen a la ubicación de destino.

| Origen | Destino |
|------|------|
| /content/fmdita | /var/dxml |
| /content/dxml | /var/dxml |
| /etc/fmdita | /libs/fmdita |

## Instalar versión 4.0 {#id23598G006XA}

1. Instale la versión 4.0 solo si los pasos de actualización se realizaron correctamente.
1. Descargar paquete de versión 4.0 de [Portal de distribución de software de Adobe](https://experience.adobe.com/#/downloads/content/software-distribution/es/aem.html):

   - Si está utilizando la versión de software de UUID, busque &quot;Versión 4.0 de UUID para la solución de XML Documentation AEM para la versión 6.5 de&quot;.
   - Si está utilizando una versión de software que no sea UUID, busque &quot;Versión 4.0 que no sea UUID para la solución XML Documentation AEM para la versión 6.5 de&quot;.
AEM Cargue el paquete en la instancia de servidor de la existente mediante el Administrador de paquetes CRX e instálelo.

   >[!NOTE]
   >
   > Espere a que se inicien todos los componentes del sistema.

1. Borre la caché del explorador después de instalar el paquete.
1. Si Dispatcher está configurado en una instancia de autor de AEM, realice los siguientes pasos:
   - Asegúrese de que se gestionan las siguientes opciones en las reglas de Dispatcher:
   - El patrón de URL /home/users/\*/preferences está en la lista blanca.
   - El patrón de URL /libs/cq/security/userinfo.json no se almacena en caché.
1. Borrar caché de Dispatcher \(para borrar cualquier `clientlibs` en caché\).

## Actualización a la versión 4.2 {#id22A3F500SXA}

AEM La actualización a la versión 4.2 depende de la versión actual de las Guías de.

Si utiliza las versiones 4.0, 4.1 o 4.1.x, puede actualizar directamente a la versión 4.2.

****Requisitos previos****

AEM Antes de iniciar el proceso de actualización de las Guías de usuario de la versión 4.2, asegúrese de que dispone de lo siguiente:

1. AEM Se ha actualizado a la versión 4.0, 4.1 o 4.1.x de las Guías de la.
1. Se cerraron todas las tareas de traducción.
1. Se ha cambiado el nivel de registro a **INFORMACIÓN** para `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` y anexar estos registros a un nuevo archivo de registro, por ejemplo, `logs/translation_upgrade.log.`

>[!NOTE]
>
> Debe cerrar todas las revisiones activas. Si las tareas de revisión no se cierran al actualizar a la versión 4.2, las tareas de revisión en curso más antiguas siguen llevando a los usuarios a las páginas de revisión más antiguas y las tareas de revisión creadas después de la actualización mostrarán las actualizaciones más recientes en la funcionalidad.

## Instalar versión 4.2 {#id2245IK0E0EV}

1. Descargar paquete de la versión 4.2 de [Portal de distribución de software de Adobe](https://experience.adobe.com/#/downloads/content/software-distribution/es/aem.html).
1. Instale el paquete de la versión 4.2.
1. Después de completar la instalación del paquete, espere a que aparezca el siguiente mensaje en los registros:

   `Completed the post deployment setup script`

   El mensaje anterior indica que se han completado todos los pasos de la instalación.

   Si encuentra cualquiera de los siguientes prefijos ERROR, informe de ellos a su equipo de éxito del cliente:

   - Error en el script de configuración posterior a la implementación
   - Excepción al transferir el mapa de traducción
   - No se puede portar el mapa de traducción de v1 a v2 para la propiedad
1. Actualice el complemento Conector de oxígeno lanzado con la versión 4.2 \(si es necesario\).
1. Borre la caché del explorador después de instalar el paquete.
1. Continúe actualizando las personalizaciones como se detalla en la siguiente sección.

## Después de instalar la versión 4.2 {#id2326F02004K}

>[!IMPORTANT]
>
> La plantilla de alta tecnología no se muestra en el servidor actualizado. Para incluir la plantilla de alta tecnología en el servidor, puede copiarla: Fuente: /libs/fmdita/pdf/Hi-Tech Destino: /content/dam/dita-templates/pdf

AEM Después de instalar las guías de la, puede combinar las distintas configuraciones aplicables desde la versión recién instalada con la configuración.

>[!NOTE]
>
> El modelo dam-update-asset se puede personalizar. AEM Por lo tanto, si se ha realizado alguna personalización, es necesario sincronizar las personalizaciones y guías de la en la copia de trabajo del modelo.

1. **Flujo de trabajo del recurso de actualización DAM \(Cambios posteriores al procesamiento\):**

1. Abrir URL:

   ```http
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html
   ```

1. Seleccionar **Flujo de trabajo de recursos de actualización DAM**.
1. Haga clic en **Editar**.
1. Si la variable **Iniciador de procesamiento posterior DXML** está presente, asegúrese de que las personalizaciones estén sincronizadas.
1. Si la variable **Iniciador de procesamiento posterior DXML** Si el componente está ausente, realice los siguientes pasos para insertarlo:

1. Clic **Insertar componente** AEM \(Responsable del procesamiento posterior de las guías de la aplicación como paso final del proceso\).
1. Configure las variables **Etapa del proceso** con los siguientes detalles:

   **Pestaña Común**

   **Título:** Iniciador de procesamiento posterior DXML

   **Descripción**: Paso del iniciador posterior del proceso DXML que almacenará en déclencheur un trabajo sling para el posprocesamiento DXML del recurso modificado/creado

   **Pestaña Proceso**

   - Seleccionar **Iniciador de procesamiento posterior DXML** desde el **Proceso** menú desplegable

   - Seleccionar **Avance del controlador**

   - Seleccionar **Listo**

1. Clic **Sincronización** en la parte superior derecha después de completar los cambios. Recibirá una notificación de éxito.

   >[!NOTE]
   >
   > AEM Actualice y verifique que los cambios personalizados y el paso posterior al procesamiento de las guías de trabajo estén presentes en el modelo final de flujo de trabajo.

1. Una **Flujo de trabajo de recursos de actualización DAM** se ha validado, compruebe las configuraciones del lanzador correspondientes. AEM Para ello, vaya a la interfaz de flujo de trabajo de la y abra los iniciadores.

   ```http
   http://localhost:4502/libs/cq/workflow/content/console.html
   ```

   Busque y realice cambios \(si es necesario\) en los dos lanzadores \(que deberían estar activos\) siguientes correspondientes a **Flujo de trabajo de recursos de actualización DAM**:

1. Lanzador para &quot;*Nodo creado*&quot; para **Flujo de trabajo de recursos de actualización DAM**- para la condición `"jcr:content/jcr:mimeType!=video"`, el valor &quot;Globbing&quot; debe ser:

   ```json
   /content/dam(/((?!/subassets|/translation_output).)*/)renditions/original
   ```

   - &#39;excludeList&#39; debería tener `"event-user-data:changedByWorkflowProcess"`.
   - Lanzador para &quot;*Nodo modificado*&quot; para **Flujo de trabajo de recursos de actualización DAM -** para la condición &quot;`jcr:content/jcr:mimeType!=video`&quot;,
   - 
      - el valor &quot;Globbing&quot; debe ser:

   ```json
   `"/content/dam(/((?!/subassets|/translation_output).)*/)renditions/original"`
   ```

   - &#39;excludeList&#39; debería tener `"event-user-data:changedByWorkflowProcess"`.
1. Una vez completada la actualización, asegúrese de que cualquiera de las personalizaciones/superposiciones se valide y actualice para que coincida con el nuevo código de la aplicación. A continuación se ofrecen algunos ejemplos:
   - Cualquier componente superpuesto de /libs/fmidator/libs debe compararse con el nuevo código de producto y las actualizaciones deben realizarse en archivos superpuestos en /apps.
   - Cualquier categoría clientlib utilizada desde el producto debe revisarse para ver si hay cambios. Cualquier configuración anulada \(ejemplos abajo\) debe compararse con las más recientes para obtener las últimas funciones:
   - elementmapping.xml
   - ui\_config.json\(puede haberse configurado en perfiles de carpeta\)
   - enmendado `com.adobe.fmdita.config.ConfigManager`
   - Compruebe si alguno de los códigos personalizados estaba utilizando rutas antiguas \(como se menciona en la [Asignación de migración](#id2244LE040XA) section\): debe actualizarse a las nuevas rutas para que las personalizaciones también funcionen según lo esperado.
1. Obtenga información acerca de las nuevas configuraciones incluidas en la versión actual \(comprobar [Notas de versión](../release-info/release-notes-4.2.md)\) y compruebe si alguna funcionalidad se ve afectada y, a continuación, tome las medidas adecuadas. Un ejemplo podría ser utilizar el &quot;Control de archivos y versiones mejorado&quot; introducido en la versión 4.0, para el cual necesita habilitar una configuración.

## Pasos para indexar el contenido existente y utilizar la nueva función de buscar y reemplazar:

Realice los siguientes pasos para indexar el contenido existente y utilice el nuevo texto de búsqueda y reemplazo a nivel de mapa:

- Ejecute una solicitud de POST al servidor \(con autenticación correcta\) - `http://<server:port\>/bin/guides/map-find/indexing`. \(Opcional: puede pasar rutas específicas de las asignaciones para indexarlas, de forma predeterminada todas las asignaciones se indexarán \|\| Por ejemplo: `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`\)

- La API devolverá un jobId. Para comprobar el estado del trabajo, puede enviar una solicitud de GET con el ID del trabajo al mismo punto final: `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(Por ejemplo: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)

- Una vez completado el trabajo, la solicitud de GET anterior responderá correctamente y mencionará si alguna asignación ha fallado. Los mapas indexados correctamente se pueden confirmar desde los registros del servidor.

## Actualización a la versión 4.2.1 {#upgrade-version-4-2-1}

AEM La actualización a la versión 4.2.1 depende de la versión actual de las Guías de.

Si utiliza la versión 4.1, 4.1.x o 4.2, puede actualizar directamente a la versión 4.2.1.

>[!NOTE]
>
>El posprocesamiento y la indexación pueden tardar unas horas. Le recomendamos que inicie el proceso de actualización durante las horas de menor actividad.

****Requisitos previos****

AEM Antes de iniciar el proceso de actualización de las Guías de usuario de la versión 4.2.1, de la versión de, asegúrese de lo siguiente:

1. AEM Se ha actualizado a la versión 4.1, 4.1.x o 4.2 de las Guías de la.
1. Se cerraron todas las tareas de traducción.
1. Se ha cambiado el nivel de registro a **INFORMACIÓN** para `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` y anexar estos registros a un nuevo archivo de registro, por ejemplo, `logs/translation_upgrade.log.`

>[!NOTE]
>
> Debe cerrar todas las revisiones activas. Si las tareas de revisión no se cierran al actualizar a la versión 4.2, las tareas de revisión en curso más antiguas siguen llevando a los usuarios a las páginas de revisión más antiguas y las tareas de revisión creadas después de la actualización mostrarán las actualizaciones más recientes en la funcionalidad.

## Instalar versión 4.2.1

1. Descargue el paquete de la versión 4.2.1 desde [Portal de distribución de software de Adobe](https://experience.adobe.com/#/downloads/content/software-distribution/es/aem.html).
1. Instale el paquete de la versión 4.2.1.
1. Puede elegir ENTRAR en el déclencheur para iniciar el trabajo de actualización del mapa de traducción. Para obtener más información, consulte [Habilitar el déclencheur del script mediante un servlet](#enable-trigger-serverlet).


1. Después de completar la instalación del paquete, espere a que aparezca el siguiente mensaje en los registros:

   `Completed the post deployment setup script`

   El mensaje anterior indica que se han completado todos los pasos de la instalación.

   Si encuentra cualquiera de los siguientes prefijos ERROR, informe de ellos a su equipo de éxito del cliente:

   - Error en el script de configuración posterior a la implementación
   - Excepción al transferir el mapa de traducción
   - No se puede portar el mapa de traducción de v1 a v2 para la propiedad
1. Actualice el complemento Conector de oxígeno lanzado con la versión 4.2 \(si es necesario\).
1. Borre la caché del explorador después de instalar el paquete.
1. Continúe actualizando las personalizaciones como se detalla en la siguiente sección.

### Habilitar el déclencheur del script mediante un servlet{#enable-trigger-serverlet}

POST:

```
http://localhost:4503/bin/guides/script/start?jobType=translation-map-upgrade
```

Respuesta:

```
{
"msg": "Job is successfully submitted and lock node is created for future reference",
"lockNodePath": "/var/dxml/executor-locks/translation-map-upgrade/1683190032886",
"status": "SCHEDULED"
}
```

En el JSON de respuesta anterior, la clave `lockNodePath` contiene la ruta al nodo creado en el repositorio que señala al trabajo enviado. Se eliminará automáticamente una vez finalizado el trabajo y, hasta entonces, puede hacer referencia a este nodo para consultar el estado actual del trabajo.

Registro de muestra: a continuación se muestra un ejemplo de registros que aparecerán en el archivo de registro después de almacenar en déclencheur la secuencia de comandos.

```
04.05.2023 14:17:12.876 *INFO* [[0:0:0:0:0:0:0:1] [1683190032736] POST /bin/guides/script/start HTTP/1.1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Acquiring lock for job : translation-map-upgrade
04.05.2023 14:17:12.897 *INFO* [pool-59-thread-1] com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Starting the thread to upgrade translation map from V1 to V2
04.05.2023 14:17:12.899 *INFO* [pool-59-thread-1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Initiating lock for node : /var/dxml/executor-locks/translation-map-upgrade/1683190032886
04.05.2023 14:17:12.901 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Starting porting of translation map from V1 to V2
04.05.2023 14:17:12.904 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Memory increase is of : 764 kB
04.05.2023 14:17:12.906 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Completed porting of translation map from V1 to V2
04.05.2023 14:17:12.907 *INFO* [pool-59-thread-1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Releasing lock for node : /var/dxml/executor-locks/translation-map-upgrade/1683190032886
04.05.2023 14:17:12.909 *INFO* [pool-59-thread-1] com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Completed the thread to upgrade translation map from V1 to V2
```

Buscar: `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Completed porting of translation map from V1 to V2` y `com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Completed the thread to upgrade translation map from V1 to V2` antes de continuar con los siguientes pasos.



## Después de instalar la versión 4.2.1

>[!IMPORTANT]
>
> La plantilla de alta tecnología no se muestra en el servidor actualizado. Para incluir la plantilla de alta tecnología en el servidor, puede copiarla: Fuente: /libs/fmdita/pdf/Hi-Tech Destino: /content/dam/dita-templates/pdf

AEM Después de instalar las guías de la, puede combinar las distintas configuraciones aplicables desde la versión recién instalada con la configuración.

>[!NOTE]
>
> El modelo dam-update-asset se puede personalizar. AEM Por lo tanto, si se ha realizado alguna personalización, es necesario sincronizar las personalizaciones y guías de la en la copia de trabajo del modelo.

1. **Flujo de trabajo del recurso de actualización DAM \(Cambios posteriores al procesamiento\):**

1. Abrir URL:

   ```http
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html
   ```

1. Seleccionar **Flujo de trabajo de recursos de actualización DAM**.
1. Haga clic en **Editar**.
1. Si la variable **Iniciador de procesamiento posterior DXML** está presente, asegúrese de que las personalizaciones estén sincronizadas.
1. Si la variable **Iniciador de procesamiento posterior DXML** Si el componente está ausente, realice los siguientes pasos para insertarlo:

1. Clic **Insertar componente** AEM \(Responsable del procesamiento posterior de las guías de la aplicación como paso final del proceso\).
1. Configure las variables **Etapa del proceso** con los siguientes detalles:

   **Pestaña Común**

   **Título:** Iniciador de procesamiento posterior DXML

   **Descripción**: Paso del iniciador posterior del proceso DXML que almacenará en déclencheur un trabajo sling para el posprocesamiento DXML del recurso modificado/creado

   **Pestaña Proceso**

   - Seleccionar **Iniciador de procesamiento posterior DXML** desde el **Proceso** menú desplegable

   - Seleccionar **Avance del controlador**

   - Seleccionar **Listo**

1. Clic **Sincronización** en la parte superior derecha después de completar los cambios. Recibirá una notificación de éxito.

   >[!NOTE]
   >
   > AEM Actualice y verifique que los cambios personalizados y el paso posterior al procesamiento de las guías de trabajo estén presentes en el modelo final de flujo de trabajo.

1. Una **Flujo de trabajo de recursos de actualización DAM** se ha validado, compruebe las configuraciones del lanzador correspondientes. AEM Para ello, vaya a la interfaz de flujo de trabajo de la y abra los iniciadores.

   ```http
   http://localhost:4502/libs/cq/workflow/content/console.html
   ```

   Busque y realice cambios \(si es necesario\) en los dos lanzadores \(que deberían estar activos\) siguientes correspondientes a **Flujo de trabajo de recursos de actualización DAM**:

1. Lanzador para &quot;*Nodo creado*&quot; para **Flujo de trabajo de recursos de actualización DAM**- para la condición `"jcr:content/jcr:mimeType!=video"`, el valor &quot;Globbing&quot; debe ser:

   ```json
   /content/dam(/((?!/subassets|/translation_output).)*/)renditions/original
   ```

   - &#39;excludeList&#39; debería tener `"event-user-data:changedByWorkflowProcess"`.
   - Lanzador para &quot;*Nodo modificado*&quot; para **Flujo de trabajo de recursos de actualización DAM -** para la condición &quot;`jcr:content/jcr:mimeType!=video`&quot;, el valor &#39;Globbing&#39; debe ser:

   ```json
   `"/content/dam(/((?!/subassets|/translation_output).)*/)renditions/original"`
   ```

   - `excludeList` debería tener `"event-user-data:changedByWorkflowProcess"`.


1. Una vez completada la actualización, asegúrese de que cualquiera de las personalizaciones/superposiciones se valide y actualice para que coincida con el nuevo código de la aplicación. A continuación se ofrecen algunos ejemplos:
   - Cualquier componente superpuesto de /libs/fmidator/libs debe compararse con el nuevo código de producto y las actualizaciones deben realizarse en archivos superpuestos en /apps.
   - Cualquier categoría clientlib utilizada desde el producto debe revisarse para ver si hay cambios. Cualquier configuración anulada \(ejemplos abajo\) debe compararse con las más recientes para obtener las últimas funciones:
   - elementmapping.xml
   - ui\_config.json\(puede haberse configurado en perfiles de carpeta\)
   - enmendado `com.adobe.fmdita.config.ConfigManager`
   - Compruebe si alguno de los códigos personalizados estaba utilizando rutas antiguas \(como se menciona en la [Asignación de migración](#id2244LE040XA) section\): debe actualizarse a las nuevas rutas para que las personalizaciones también funcionen según lo esperado.
1. Obtenga información acerca de las nuevas configuraciones incluidas en la versión actual \(comprobar [Notas de versión](../release-info/release-notes-4.2.1.md)\) y compruebe si alguna funcionalidad se ve afectada y, a continuación, tome las medidas adecuadas. Un ejemplo podría ser utilizar el &quot;Control de archivos y versiones mejorado&quot; introducido en la versión 4.0, para el cual necesita habilitar una configuración.

## Pasos para indexar el contenido existente y utilizar la nueva función de buscar y reemplazar:

Realice los siguientes pasos para indexar el contenido existente y utilice el nuevo texto de búsqueda y reemplazo a nivel de mapa:

- Asegúrese de que la variable `damAssetLucene` se ha completado la indexación. Puede tardar hasta unas horas, según la cantidad de datos presentes en el servidor. Puede confirmar que la reindexación se ha completado comprobando que el campo de reindexación está configurado como falso en
   `http://<server:port>/oak:index/damAssetLucene`.  Además, si ha añadido personalizaciones en `damAssetLucene`, es posible que tenga que volver a aplicarlos.

- Ejecute una solicitud de POST al servidor \(con autenticación correcta\) - `http://<server:port\>/bin/guides/map-find/indexing`. (Opcional: puede pasar rutas específicas de las asignaciones para indexarlas, de forma predeterminada, todas las asignaciones se indexarán \|\| Por ejemplo: `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

- También se puede pasar una carpeta raíz para indexar las asignaciones DITA de una carpeta específica (y sus subcarpetas). Por ejemplo, `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test`. Tenga en cuenta que si se pasan tanto el parámetro de rutas como el parámetro raíz, solo se tendrá en cuenta el parámetro de rutas.

- La API devolverá un jobId. Para comprobar el estado del trabajo, puede enviar una solicitud de GET con el ID del trabajo al mismo punto final: `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(Por ejemplo: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)


- Una vez completado el trabajo, la solicitud de GET anterior responderá correctamente y mencionará si alguna asignación ha fallado. Los mapas indexados correctamente se pueden confirmar desde los registros del servidor.

**Tema principal:**[ Descargar e instalar](download-install.md)
