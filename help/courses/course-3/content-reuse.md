---
title: Reutilización de contenido
description: Uso recurrente de funciones en AEM Guides
exl-id: 453c5a09-0bcf-4760-87fc-df3ea4a3a30a
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 1%

---

# Reutilización de contenido

Una de las características principales de DITA es la capacidad de reutilizar contenido. Permite reutilizar contenido desde frases pequeñas hasta temas o mapas completos.  Sin embargo, para que el contenido se reutilice de forma eficaz, debe administrarse correctamente. Asegúrese de tener una estrategia de contenido eficaz al trabajar con información reutilizable.

>[!VIDEO](https://video.tv.adobe.com/v/342757?quality=12&learn=on)

## Crear un tema reutilizable

Cuando se realiza un cambio en un tema de origen reutilizable, la información se actualiza siempre que se utiliza el contenido.

1. Vaya a **Repositorio**.

1. Haga clic en el **menú contextual** junto a la carpeta de reutilización.

1. Elija **Crear > Tema Dita**.

1. Rellene los campos en el cuadro de diálogo Crear nuevo tema. Por ejemplo:

   ![Confirmación](images/lesson-8/new-topic-dialog.png)

1. Haga clic en [!UICONTROL **Crear**].

1. Agregue contenido al tema según sea necesario.

## Añadir un nuevo elemento reutilizable a un tema

Existen varios métodos para añadir elementos reutilizables. En este caso, el primer flujo de trabajo es mejor cuando se añade solo un componente. El segundo flujo de trabajo es mejor para añadir varios componentes reutilizables.

### Flujo de trabajo 1

1. Haga clic en el tema en una ubicación válida.

1. Seleccione el icono **Insertar contenido reutilizable** en la barra de herramientas superior.

   ![Confirmación](images/lesson-8/insert-reuse-icon.png)

1. En el diálogo Reutilizar contenido, haga clic en el icono [!UICONTROL **Carpeta**].

1. Vaya a la carpeta requerida.

1. Elija un tema con componentes reutilizables.
Por ejemplo:

   ![Confirmación](images/lesson-8/reusable-topic.png)

1. Haga clic en [!UICONTROL **Seleccionar**].

1. Elija un componente específico para reutilizarlo.

1. Haga clic en [!UICONTROL **Seleccionar**].

El elemento reutilizable ahora se ha insertado en el tema.

### Flujo de trabajo 2

1. Vaya a **Contenido reutilizable** en el panel izquierdo.

1. Haga clic en el icono [!UICONTROL **Agregar**] en el panel Contenido reutilizable.

   ![Confirmación](images/lesson-8/reuse-contents-icon.png)

1. Vaya a una carpeta.

1. Seleccione uno o varios temas específicos.

1. Haga clic en [!UICONTROL **Agregar**].

1. En el panel Contenido reutilizable, expanda **Información general del elemento**.

1. Arrastre y suelte un elemento en el tema en una ubicación válida.

El elemento reutilizable ahora se ha insertado en el tema.

## Asignar un ID y un valor a un elemento

La dlentry que acaba de crear es un elemento reutilizable. Por lo tanto, requiere un ID y un valor.

1. Haga clic dentro de la dlentry.

1. En el panel Propiedades del contenido, haga clic en el menú desplegable situado debajo de Atributo.

1. Seleccione **ID**.

1. Escriba un nombre lógico para el valor.

1. Guarde o convierta en versión el tema para que el cambio se refleje en el Repositorio.

El ID y el valor se han asignado al elemento.
