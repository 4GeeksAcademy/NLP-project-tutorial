<!-- hide -->
# SVM para detectar spam en enlaces - Guía paso a paso
<!-- endhide -->

- Comprender un dataset nuevo.
- Modelar los datos utilizando un SVM.
- Analizar los resultados y optimizar el modelo.

## 🌱  Cómo iniciar este proyecto

Esta vez no se hará Fork, tómate un tiempo para leer estas instrucciones:

1. Crear un nuevo repositorio basado en el [proyecto de Machine Learing](https://github.com/4GeeksAcademy/machine-learning-python-template/generate) [haciendo clic aquí](https://github.com/4GeeksAcademy/machine-learning-python-template).
2. Abre el repositorio creado recientemente en Codespace usando la [extensión del botón de Codespace](https://docs.github.com/en/codespaces/developing-in-codespaces/creating-a-codespace-for-a-repository#creating-a-codespace-for-a-repository).
3. Una vez que el VSCode del Codespace haya terminado de abrirse, comienza tu proyecto siguiendo las instrucciones a continuación.

## 🚛 Cómo entregar este proyecto

Una vez que hayas terminado de resolver los ejercicios, asegúrate de confirmar tus cambios, hazle "push" al fork de tu repositorio y ve a 4Geeks.com para subir el enlace del repositorio.

## 📝 Instrucciones

### Sistema de detección de enlaces spam

Queremos implementar un sistema que sea capaz de detectar automáticamente si una página web contiene spam o no basándonos en su URL.

#### Paso 1: Carga del conjunto de datos

El conjunto de datos se puede encontrar en esta carpeta de proyecto bajo el nombre `url_spam.csv`. Puedes cargarlo en el código directamente desde el enlace (`https://raw.githubusercontent.com/4GeeksAcademy/NLP-project-tutorial/main/url_spam.csv`) o descargarlo y añadirlo a mano en tu repositorio.

#### Paso 2: Preprocesa los enlaces

Utiliza lo visto en este módulo para transformar los datos para compatibilizarlos con el modelo que queremos entrenar. Segmenta las URLs en partes según sus signos de puntuación, elimina las stopwords, lematiza, etcétera.

Asegúrate de dividir convenientemente el conjunto de datos en `train` y `test` como hemos visto en lecciones anteriores.

#### Paso 3: Construye un SVM

Comienza a resolver el problema implementando un SVM con los parámetros por defecto. Entrénalo y analiza sus resultados.

#### Paso 4: Optimiza el modelo anterior

Después de entrenar el SVM, optimiza sus hiperparámetros utilizando un grid search o un random search.

#### Paso 5: Guarda el modelo

Almacena el modelo en la carpeta correspondiente.

> NOTA: Solución: https://github.com/4GeeksAcademy/NLP-project-tutorial/blob/main/solution.ipynb