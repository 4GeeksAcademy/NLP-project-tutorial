<!-- hide -->
# NLP Project Tutorial
<!-- endhide -->

- En nuestro último cuaderno de exploración de NLP, construimos un detector de spam de correo electrónico utilizando técnicas de procesamiento de lenguaje natural y el algoritmo Support Vector Machine (SVM) para la clasificación.

- En este proyecto, construiremos nuevamente un detector de spam, pero esta vez usando URL en lugar de correos electrónicos.

## 🌱  Cómo iniciar este proyecto

Esta vez no se hará Fork, tómate un tiempo para leer estas instrucciones:

1. Crear un nuevo repositorio basado en el [proyecto de Machine Learing](https://github.com/4GeeksAcademy/machine-learning-python-template/generate) [haciendo clic aquí](https://github.com/4GeeksAcademy/machine-learning-python-template).
2. Abre el repositorio creado recientemente en Gitpod usando la [extensión del botón de Gitpod](https://www.gitpod.io/docs/browser-extension/).
3. Una vez que Gitpod VSCode haya terminado de abrirse, comienza tu proyecto siguiendo las instrucciones a continuación.

## 🚛 Cómo entregar este proyecto

Una vez que hayas terminado de resolver los ejercicios, asegúrate de confirmar tus cambios, hazle "push" a el fork de tu repositorio y ve a 4Geeks.com para subir el enlace del repositorio.

## 📝 Instrucciones

**Detector de spam de URL**

Usaremos un conjunto de datos de URL que puedes encontrar en el siguiente enlace https://raw.githubusercontent.com/4GeeksAcademy/NLP-project-tutorial/main/url_spam.csv

**Paso 1:**

Carga tu conjunto de datos y realiza las transformaciones necesarias en tu variable de destino.

**Paso 2:**

Utiliza técnicas de PNL para preprocesar los datos.
Aquí hay otra idea sobre cómo excluir algunas palabras creando nuevas columnas:

```py
df['len_url'] = df['url'].apply(lambda x : len(x))
df['contains_subscribe'] = df['url'].apply(lambda x : 1 if "subscribe" in x else 0)
df['contains_hash'] = df['url'].apply(lambda x : 1 if "#" in x else 0)
df['num_digits'] = df['url'].apply(lambda x : len("".join(_ for _ in x if _.isdigit())) )
df['non_https'] = df['url'].apply(lambda x : 1 if "https" in x else 0)
df['num_words'] = df['url'].apply(lambda x : len(x.split("/")))

target = 'is_spam'
features = [f for f in df.columns if f not in ["url", target]]
X_train, X_test, y_train, y_test = train_test_split(df[features], df[target], test_size=0.2, random_state=0)
```

**Paso 3:**

Utiliza la máquina Support Vector para crear un clasificador de spam de URL.

**Paso 4:**

Como siempre, usa tu notebook para experimentar y asegúrese de obtener los resultados que deseas.

Usa tu archivo app.py para guardar tus pasos definidos, pipelines o funciones en el orden correcto.

En tu archivo README escribe un breve resumen.

Guía de soluciones: 

https://github.com/4GeeksAcademy/NLP-project-tutorial/blob/main/solution_guide.ipynb
