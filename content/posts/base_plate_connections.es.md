---
title: "Uniones a la cimentación: Una guía conceptual"
date: 2025-05-18T23:27:03+02:00
draft: false
cover:
  image: img/cover/base_plate_cover.jpg
  thumbnail: img/thumbs/base_plate_thumbnail.jpg
tags: ["acero", "estructura", "soportes", "placa base"]
categories: ["Estructuras de acero"]
author: ["MHS"]
authorImage: "img/authors/MHS.jpg"
---

En este artículo exploramos los fundamentos de las **uniones acero–hormigón**, con un enfoque particular en las uniones de placa base. Entender los **conceptos fundamentales** de la mecánica que rige estas conexiones, podemos navegar las normas y códigos de diseño aplicables con mayor claridad y confianza.

## ¿Cómo funcionan las uniones de placa base?

En esencia, sin importar que hipótesis tomemos a la hora de modelar nuestra estructura, el **objetivo** siempre es el mismo: **garantizar** que cada componente resista de forma segura las cargas aplicadas cuñpliendo con los **criterios de servicio y de seguridad** durante su vida útil.

> 📍 No se trata de perseguir la complejidad, sino de **alinear** nuestras **hipótesis de diseño con el sistema físico**.

Pongamos en contexto. Supongamos que hemos finalizado nuestro análisis estructural: el modelo de Elementos Finitos (FEA) está terminado, las verificaciones de los miembros estructurales han sido finalizadas, seleccionando las secciones adecuadas para vigas y columnas. Las reacciones en los apoyos, fuerzas y momentos, han sido calculadas. Ahora la **atención** se dirige a una **parte crucial pero frecuentemente subestimada: los soportes** en sí mismos.

Ya sabemos qué **cargas** debe ser capaz de transmitir cada apoyo hacia la fundación o muro al que está vinculado. El siguiente paso es **diseñar** esa **interfaz de conexión** de forma tal que refleje las **suposiciones** adoptadas en el modelo, especialmente en lo que respecta a las **condiciones de borde** (CBs). Generalmente, estas condiciones se clasifican en dos **categorías**:

- **Empotrado** (fijo): No se permiten desplazamientos ni rotaciones. Se restringen los seis grados de libertad (UX, UY, UZ, RX, RY, RZ), permitiendo la **transferencia completa de fuerzas y momentos**.

- **Articulado**: Solo se permite la rotación. Se restringen los desplazamientos (UX, UY, UZ), pero **no hay transferencia de momentos**.

>💡 El comportamiento real se encuentra en algún punto entre estos dos extremos: Ningún apoyo es perfectamente articulado ni absolutamente rígido.

Como **ingenieros.as**, nuestra tarea es **diseñar** los **componentes** (placa base, pernos, mortero, fundación de hormigón) **con el fin de obtener una respuesta del sistema coherente con nuestras suposiciones de modelado**, dentro de las tolerancias constructivas, los márgenes de seguridad y el costos previstos.

## Anatomía de un empotramiento: elementos que lo componen

> 💡 ¿Qué función debe cumplir el apoyo? ¿Solo transmitir cargas axiales? ¿Debe también resistir momentos flectores? ¿Se requieren refuerzos para mejorar su desempeño?

Estas son algunas de las **preguntas que debemos hacernos** al comenzar el diseño de una unión acero–hormigón. Si bien la información inicial, en forma de reacciones, proviene del modelo de Elementos Finitos (FEA), estos datos solo son útiles si comprendemos cómo funciona el sistema de apoyo y cómo está compuesto.

Se trata de decidir qué componentes son esenciales para lograr la respuesta estructural requerida y asegurarse de invertir tiempo en aquellos que realmente contribuyen al desempeño del sistema.

>📌 El **diseño en ingeniería** no es solo cálculo, también **es criterio**. 

Nuestro trabajo consiste en **guiar el flujo de esfuerzos** desde la columna hacia los elementos intermedios, como la **placa base**, los **pernos** y el **mortero**, hasta llegar finalmente a la **fundación** de hormigón.

Antes de comenzar a dimensionar, debemos **identificar** los posibles **elementos** que puede incluir este tipo de sistemas. Solo así podremos determinar cuáles son **necesarios para nuestro caso particular**. Este proceso suele ser iterativo: pueden surgir nuevos requerimientos durante el diseño, y esto es totalmente normal. La fase de diseño siempre deja margen para ajustes y para volver sobre nuestros pasos en busca de coherencia entre modelos y factibilidad.

Las **uniones a la cimentación** pueden variar según las demandas estructurales y las preferencias constructivas. Sin embargo, los siguientes **componentes** son **comunes** en la mayoría de las configuraciones:

![Conexion_Empotrado_Articulado.jpg](/img/posts/Conexion_Empotrado_Articulado.jpg)

- **Columna** (Perfil): **Transfiere** los **esfuerzos y/o momentos internos** hacia el apoyo. Ya ha sido diñensionado y verificado en etapas anteriores.
    
- **Placa Base**: **Distribuye** las **cargas de compresión** provenientes de la columna sobre un área mayor y las transfiere a la fundación.

- **Unión perfil–placa**: **Une el perfil con la placa base**. Según el tipo de condición de borde:
    
    - En apoyos empotrados (fijos) → *Soldadura de filete*
    - En apoyos articulados → *Pernos de conexión*

- **Mortero** (grouting): Asegura la **nivelación** de la estructura, una **superficie de apoyo uniforme** y transfiere las fuerzas de **compresión** desde la placa al hormigón.

- **Fundación de hormigón**: **Recibe** el **flujo final de cargas** del sistema de apoyo.
    
- **Rigidizadores** *(Opcional)*: **Se utilizan cuando existen grandes momentos flectores**.
    
- **Perfil Conector** *(Opcional)*: **Ayuda a resistir esfuerzos cortantes elevados** transmitidos desde la placa base.

## ¿Cómo se comportan las uniones de placa base bajo carga?

Antes de hablar siquiera de la resistencia de los componentes, debemos entender qué puede estar ocurriendo en la unión bajo ciertas solicitaciones.

Consideremos una **unión empotrada** sometida a fuerzas y momentos en las direcciones X, Y y Z, como se muestra en la siguiente figura:
![Fixed Base plate.jpg](/img/posts/Fixed_Base_plate.jpg)

Así como el relieve del terreno condiciona el flujo del agua cuesta abajo, la configuración geométrica y la rigidez de una estructura determinan cómo fluyen los esfuerzos internos a través de ella. Las **fuerzas**, al igual que el agua, **tienden a seguir las trayectorias de menor resistencia**, cuyo análogo estructural corresponde a los **elementos de mayor rigidez y continuidad**.

>💡 Podemos pensar en la **rigidez** como el **medio a través del cual fluyen las fuerzas**.

Para que la **placa base** funcione correctamente, ésta **debe tener suficiente rigidez** para permitir que las esfuerzos fluyan hacia donde queremos. Los siguientes esquemas ilustran cómo la rigidez de la placa puede afectar la transferencia de cargas hacia los pernos y el hormigón, en algunos casos de solicitaciones elementales:

![Rigidez_placa_base.jpg](/img/posts/Rigidez_placa_base.jpg)
📌 Más sobre la rigidez de los soportes acá : [Insert link to blog entry] 

La placa base “recoge” los esfuerzos internos del perfil y las transfiere a los pernos y al hormigón.

>💡 En esencia, **la placa actúa como un nodo de transferencia de esfuerzos**.

Comprender las interacciones en cada interfaz es clave para garantizar que el sistema se comporte como queremos, en particular si queremos asegurarnos de que las hipótesis adoptadas en el modelado por elementos finitos (como soportes rígidos, semi-rígidos o flexibles) se respeten.

La siguiente tabla resume las interacciones entre componentes en un sistema de unión empotrada:

| **Interfaz** | **Tranferencia de Esfuerzos** | **Comentarios** |
| --- | --- | --- |
| Perfil-Placa | Tracción, Compresión, Corte, Flexión, Torsión | Soldaduras de filete para conexiones empotradasnections. |
| Rigidizadores-Placa | Compresión, Flexión | Aumentan la superficie de apoyo en compresión y el brazo de palanca z, mejorando la capacidad de transmitir compresión y momento. Su resistencia no está explícitamente incluida en normativas como el EC3. |
| Placa-Hormigón | Compresión, Corte (por fricción) | La fricción suele despreciarse, ya que no se espera movimiento relativo una vez instalada la unión. |
| Placa-Pernos | Tracción, Corte | La torsión se transfiere desde la placa a los pernos en forma de esfuerzo cortante. |
| Pernos-Hormigón | Tracción, Corte | Anclajes químicos (por adherencia) o mecánicos (por expansión). |
| Conector-Hormigón | Corte | El perfil conector transmite grandes esfuerzos cortantes directamente a la fundación. |

En una unión empotrada, la interfaz principal es la de **perfil a placa**, donde se transfieren los esfuerzos internos (**axiales, cortantes y momentos flectores**) desde el perfil estructural hacia la placa. En sistemas empotrados, esta conexión se logra habitualmente mediante cordones de **soldadura de filete**, que aseguran la continuidad entre piezas y la **transmisión** tanto de **fuerzas** como de **momentos**.

Desde la placa, las cargas se redistribuyen hacia tres elementos principales: los **rigidizadores** (si están presentes), los **pernos de anclaje** y la **fundación de hormigón**. Veamos cada interfaz por separado:

- La interfaz **placa–hormigón** transmite principalmente **compresión**, ya que la placa apoya directamente sobre la base (a menudo a través de una capa de mortero de nivelación). Aunque en teoría la fricción entre la platina y el hormigón podría ayuda a resistir esfuerzos cortantes en el plano, este efecto solo es relevante en apoyos simples, y suele despreciarse en uniones empotradas.

- Si existen **rigidizadores**, actúan como **redistribuidores locales de carga**, especialmente bajo **momentos elevados**. **Aumentan** tanto la **superficie efectiva de apoyo** como el **brazo de palanca z** (ver EN 1993 §6.2.8), mejorando la resistencia a flexión de la placa y la capacidad de apoyo local. Aunque su verificación no está incluida explícitamente en las fórmulas del EC3, su uso es ampliamente reconocido en la práctica.

- La interfaz **placa–pernos** es fundamental para la **transmisión** de **tracción**, **corte** e incluso **efectos torsionales**. En una conexión empotrada, la placa tira o empuja sobre los pernos, generando tracción y/o corte en función de solicitaciones. Los esfuerzos torsionales se transfieren como corte al grupo de pernos.

- La interfaz **pernos–hormigón** es el último eslabón de la cadena resistente. Aquí, los esfuerzos de **tracción y corte** deben transmitirse con fiabilidad **a la cimentación**.

- Finalmente, la interfaz **conector–hormigón** es clave cuando se deben resistir **grandes esfuerzos de corte**. En estos casos, no es práctico depender solo de los pernos, ya que los diámetros requeridos pueden resultar poco viables o costosos. Un perfil conector (o tope) proporciona una solución robusta para **transmitir el corte directamente al hormigón**.

## Modos de Fallo Típicos

La resistencia de diseño del sistema está gobernada por el componente con la menor capacidad resistente. Cada elemento del sistema debe evaluarse por separado para determinar su resistencia específica.

>💡 La unión es tan fuerte como su eslabón más débil.

### Placa base

Como se explicó anteriormente, la placa base debe tener un tamaño, una rigidez y una resistencia suficientes para transferir las cargas aplicadas tanto a los pernos de anclaje como a la fundación de hormigón, sin exceder las capacidades de los materiales ni las tolerancias geométricas. Dos **modos de ruina principales** suelen regir su diseño:

- **Área de apoyo insuficiente**: Cuando la placa es demasiado pequeña, **no puede distribuir eficazmente las fuerzas de compresión**. Esto genera tensiones de apoyo excesivas sobre la superficie del hormigón, que pueden superar la resistencia de diseño admisible definida por la EN 1992 y referenciada por la EN 1993.

- **Espesor insuficiente**: Si la placa es demasiado delgada, puede **no resistir los momentos flectores** inducidos por cargas excéntricas. Esto es particularmente relevante en conexiones empotradas, donde la placa actúa como un voladizo entre las alas del perfil de la columna y la superficie del hormigón.

Un dimensionamiento preciso del área de contacto y del espesor de la placa es esencial para garantizar una transferencia eficaz de cargas y mantener la coherencia con las condiciones de borde asumidas en los modelos de elementos finitos.

### Pernos de Anclaje y Hormigón

Los siguientes esquemas ilustran los modos de fallo más comunes que afectan a los pernos de anclaje y al hormigón en conexiones con placa base. Se deben considerar dos tipos principales de esfuerzos: **tracción y corte**. Cada tipo afecta de manera distinta a los componentes de acero y hormigón, por lo que deben verificarse por separado.

![Modos de falla por tensión.jpg](/img/posts/Modos_de_falla_por_tensión.jpg)

- **Acero (pernos de anclaje)**:

    - **Rotura por tracción del perno**: Se produce si el área de la **sección transversal** del perno es **insuficiente** para resistir la fuerza de tracción aplicada.

    - **Extracción**: Ocurre cuando la **adhesión** (anclajes químicos) o la **fuerza de expansión** del perno de mecánico son **insuficientes** para mantener el perno en su lugar.

- **Hormigón**:

    - **Rotura por cono de hormigón**: Un modo común en el que se forma un cono de rotura si la **profundidad de empotramiento** es muy **reducida** o si la **tensión de tracción en el hormigón supera su resistencia**. Afecta tanto a anclajes mecánicos como químicos.

    - **Rotura por descascarado de hormigón**: En el caso de anclajes mecánicos, una **espesor insuficiente del hormigón** puede provocar una falla localizada cerca de la zona de expansión del perno.

![Modos de falla por corte.jpg](/img/posts/Modos_de_falla_por_corte.jpg)

- **Acero (pernos de anclaje)**:

    - **Rotura por corte**: Causada por una **sección transversal** del perno **insuficiente** para resistir la fuerza cortante.

    - **Flexión del perno** (en platinas sin mortero): Cuando no hay mortero de nivelación, los pernos pueden actuar como voladizos, y el momento flector excesivo puede provocar fluencia del acero.

- **Hormigón**:

    - **Rotura por palanca** (arrancamiento): Ocurre cuando la profundidad de anclaje es insuficiente, haciendo que se desprenda un bloque de hormigón por acción de palanca.

    - **Rotura del borde**: Si los anclajes están colocados demasiado cerca del borde, las fuerzas de corte pueden hacer que se desprenda una cuña de hormigón debido a efectos de brazo de palanca.

📌 Para más información sobre los tipos de anclajes y consideraciones de instalación, consultá: [Anchor Fastening Technical Guide (Hilti North America)](https://viewer.joomag.com/product-technical-guides-us-en-anchor-fastening-august-2021/0929173001570655195/p1?short=)

---

## Resumen

> 💡 Ya sea que estemos dimensionando nuestra primera placa base o afinando un sistema de anclaje complejo, una buena base conceptual es nuestra herramienta de diseño más valiosa.

El diseño de uniones a la cimentación no se trata sólo de insertar valores en formulas: se trata de comprender cómo se transmiten las cargas a través de los materiales, cómo interactúan los distintos componentes entre sí, y saber dónde pueden surgir puntos débiles.

Al descomponer el sistema en elementos fundamentales y analizar su comportamiento ante diferentes solicitaciones, podemos tomar mejores decisiones de diseño desde el principio.

- **Ante la duda, dibujá un diagrama de cuerpo libre**: Representar las interacciones entre los componentes, desde el perfil hasta la fundación, ayuda a entender el rol que juega cada componente.

- **No subestimar el comportamiento del hormigón**: Los modos de fallos en el hormigón, como el desprendimiento en forma de cono, el arranque por palanca o la rotura en el borde, pueden ser tan críticos como las fallas en el acero, especialmente cuando hay profundidades de anclaje reducidas o espaciamientos insuficientes.

- **Evitá depender en exceso de las herramientas de software**: Aplicaciones como IDEA StatiCa o Tekla Tedds son excelentes ayudas al diseño, pero deben estar sustentadas en el criterio del usuario y en una comprensión clara de los supuestos que utilizan. En caso de duda, nunca está de más hacer verificaciones con cálculos manuales o modelos simplificados.

- **Respetar los criterios de montaje establecidos por las guias y normas**: Las distancias mínimas al borde, entre ejes de bulones, de profundidad de anclaje y los espesores mínimos de placa están definidos por una razón: garantizan la seguridad, durabilidad y el rendimiento.

---

## Referencias

**EN 1993-1-8**:

European Committee for Standardization. (2005). *EN 1993-1-8: Eurocode 3 – Design of steel structures – Part 1-8: Design of joints*. Brussels: CEN.

**EN 1992** (general reference to EN 1992-1-1, most commonly used):

European Committee for Standardization. (2004). *EN 1992-1-1: Eurocode 2 – Design of concrete structures – Part 1-1: General rules and rules for buildings*. Brussels: CEN.

European Organization for Technical Approvals. (2013). ***ETAG 001**: Guideline for European Technical Approval of Metal Anchors for Use in Concrete – Part 1: Anchors in General* (Edition 1997, 1st amended 2006, 2nd amended 2013). EOTA.

Celigüeta, J. T., & Tecnun (Universidad de Navarra). (2022). *Diseño de estructuras de acero. Uniones*. [CC BY-NC-SA 3.0 ES]. [https://creativecommons.org/licenses/by-nc-sa/3.0/es/](https://creativecommons.org/licenses/by-nc-sa/3.0/es/)