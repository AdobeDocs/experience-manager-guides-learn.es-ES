---
title: Publicación de un tema en un fragmento de contenido
description: Obtenga información sobre cómo publicar un tema en un fragmento de contenido.
source-git-commit: 6cd7d2ec76f90a192dbcd0ef552789d42c23a4fb
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 1%

---


# Publicación en un fragmento de contenido

AEM Los fragmentos de contenido son fragmentos de contenido discretos en el espacio de trabajo de la. Son contenidos estructurados basados en un modelo de contenido. Los fragmentos de contenido son contenido puro sin información de diseño. AEM Se pueden crear y administrar de forma independiente de los canales que admite el usuario en la aplicación de la. Los fragmentos de contenido son modulares, donde el contenido se desglosa en componentes más pequeños.

AEM Guías de le permite publicar un tema o los elementos dentro de un tema en un fragmento de contenido. Puede crear una asignación basada en JSON entre un tema y un modelo de fragmento de contenido. Utilice esta asignación para publicar un tema o los elementos dentro de un tema en un fragmento de contenido. AEM A continuación, puede utilizar fragmentos de contenido en cualquier sitio de contenido o extraer los detalles mediante las API admitidas por los fragmentos de contenido.


Para crear un fragmento de contenido, realice los siguientes pasos:

1. Crear un [modelo de fragmento de contenido](https://experienceleague.adobe.com/docs/experience-manager-65/assets/content-fragments/content-fragments-models.html?lang=es) en AEM Assets.
1. Cree una carpeta en la que desee guardar los fragmentos de contenido que cree en función del modelo de fragmento de contenido. Por ejemplo, &quot;stock-content-fragments&quot;.
1. Edite las propiedades de la carpeta (por ejemplo, &quot;stock-content-fragments&quot;) y agregue la ruta de la carpeta, que contiene el modelo de fragmento de contenido en la configuración de la nube.
Por ejemplo, añada `/conf/we-retail` en la configuración de nube. Esta configuración conecta todos los modelos de fragmento de contenido con la carpeta.\
   ![añada detalles de configuración de nube en las propiedades de la carpeta](images/fragment-folder-cloud-configuration.png){width="650" align="left"}
   *Agregue la configuración de nube en las propiedades de la carpeta para conectarla con los modelos de fragmento.*
1. Seleccione el tema que desea publicar en la **Vista de repositorio**.
1. Desde el **Opciones** menú, seleccione **Publicar como** > **Fragmento de contenido**.
1. En el **Publicar como fragmento de contenido** , rellene los siguientes detalles:
   ![Agregue el modelo de fragmento y los detalles de asignación en el cuadro de diálogo Publicar como fragmento de contenido](images/content-fragment-publish.png){width="500" align="left"}
   *Agregue la ruta, el modelo y los detalles de asignación para publicar un tema o sus elementos como fragmento de contenido. Puede sobrescribir un fragmento de contenido existente.*

   * **Ruta**: busque y seleccione la ruta de la carpeta en la que desea publicar el fragmento de contenido. También puede seleccionar un fragmento de contenido existente y publicarlo.
   * **Título**: introduzca el título del fragmento de contenido.
   * **Nombre**: introduzca el nombre del fragmento de contenido.
   * **Modelo**: seleccione el modelo de fragmento de contenido que desea utilizar para crear el fragmento de contenido. Los modelos se seleccionan de la carpeta que ha configurado en los servicios en la nube.
   * **Asignación**: seleccione una asignación en la lista desplegable. Selecciona las asignaciones de la variable *contentFragmentMapping.json* archivo.

     >[!NOTE]
     >
     >El administrador puede añadir las asignaciones en la *contentFragmentMapping.json* archivo.  Obtenga más información sobre cómo [creación de una asignación entre un tema y un fragmento de contenido](../install-guide/conf-content-fragment-mapping.md) in *Guía de instalación y configuración On-Premise*.


   * Seleccione el **Sobrescribir** casilla de verificación si el fragmento de contenido ya existe y desea sobrescribirlo. AEM Guías de contenido muestra un error si no selecciona la casilla de verificación y el fragmento de contenido ya existe.
1. Clic **Crear** para publicar el fragmento de contenido.
1. Puede ver los fragmentos de contenido de un tema en la sección **Fragmentos** de la sección **Propiedades del archivo**.

   ![Ver los fragmentos de contenido de un tema](images/topic-content-fragments.png){width="300" align="left"}

   *Vea los fragmentos de contenido presentes para un tema y vuelva a publicarlos.*

También puede volver a publicar el fragmento de contenido para actualizar el fragmento de contenido con el contenido más reciente del tema DITA.



AEM Una vez publicados los fragmentos de contenido, también puede utilizarlos en cualquier sitio de la.
