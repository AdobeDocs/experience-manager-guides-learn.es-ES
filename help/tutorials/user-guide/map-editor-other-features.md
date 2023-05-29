---
title: Otras funciones de los editores de mapas
description: Aprenda a utilizar otras funciones en los editores de mapas
exl-id: ed6f42f6-b95e-4c4d-a648-6f29641a3488
source-git-commit: 8073716bccacbe8d6a158b44d5106b083e3a5dcd
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Otras funciones de los editores de mapas {#id1942D0T0HUI}

Algunas funciones comunes de los editores de mapas básicos y avanzados son:

## Resolver referencias clave {#id176GD01H05Z}

Una referencia de clave de contenido DITA, o `conkeyref` es un mecanismo para insertar una parte del contenido de un tema en otro. Este mecanismo utiliza claves para localizar el contenido que se va a reutilizar, en lugar del mecanismo de referencia de contenido directo. Para obtener más información sobre las referencias directas e indirectas en DITA, consulte *Direccionamiento DITA* en Especificación del lenguaje DITA de OASIS.

Si el tema DITA tiene referencias clave asociadas, deben resolverse antes de obtener una vista previa, editar o revisar un tema.

Las referencias clave se resuelven en función del mapa raíz establecido en el siguiente orden de prioridad:

1. Preferencias de usuario
1. Panel Vista de mapa
1. Perfil de carpeta

El mapa raíz seleccionado en Preferencias de usuario tiene la prioridad más alta para resolver las referencias clave seguidas del panel Vista de mapa y el mapa raíz Perfil de carpeta. Por lo tanto, si no se define ningún mapa en las Preferencias del usuario, se utilizará el mapa abierto en el panel Vista de mapa. Si no se abre ninguna asignación en el panel Vista de mapa, se utiliza el conjunto de asignaciones de los Perfiles de carpeta para resolver las referencias clave.

Las referencias clave se pueden almacenar en un fichero de mapa DITA o en un fichero DITA independiente. AEM En las guías de la, puede especificar referencias clave en el nivel de proyecto o de sesión. Si ya se ha definido un mapa raíz para la sesión del usuario, se utilizará para resolver las claves. De lo contrario, se utiliza el mapa raíz predeterminado para esa carpeta. Si no se configura un mapa raíz predeterminado, las referencias clave que faltan se resaltan al usuario.

Existen varias formas de resolver referencias clave en un tema DITA mediante la definición del mapa DITA que se utilizará en las siguientes ubicaciones:

**Propiedades del proyecto** : puede definir un mapa raíz para resolver referencias clave al crear un proyecto en la sección Propiedades del proyecto.

Esta asignación raíz se aplicará a todos los recursos \(carpetas y subcarpetas\) asociados a ese proyecto. Para el contenido al que se hace referencia en varios proyectos, se mantiene una lista alfabética de proyectos y se utiliza el mapa raíz predeterminado asociado al primer proyecto. También se puede elegir el mapa DITA que se utilizará de la lista para resolver referencias clave.

**Previsualización del tema** : en el modo de vista previa del tema, pulse en el icono Resolución de clave de la barra de herramientas y seleccione el fichero DITA que se utilizará para las referencias de clave.

**Vista de edición de temas** : pulse en el icono Resolución de claves mientras edita un tema DITA y seleccione el fichero DITA que se utilizará para resolver las referencias de claves.

**Tema principal:**[ Trabajo con el editor de mapas](map-editor.md)