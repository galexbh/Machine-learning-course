# Setup del curso

En este curso utilizaremos Jupyter Notebooks y el stack Pydata, que incluye las librerías Numpy, Pandas, Matplotlib y Scikit-learn.

En lo que sigue te presento 3 opciones para trabajar con estas tecnologías:

1. Trabajar en el cloud gracias a la excelente herramienta **Google Colab**.
2. Trabajar en local en tu computadora gracias a **Anaconda**.
3. Trabajar en tu computadora virtualizando a través de contenedores con **Docker**.

**Google Colab es la opción mas facil de usar, así que esta es la opción oficial recomendada por el curso.**

Solo lee las instrucciones para las otras opciones si por alguna razon en particular prefieres ocupar una de ellas (Anaconda permite que trabajes en local, y Docker es bueno para usos en producción).

## Google Colab

Google Colab es muy similar en su uso a Google Docs. Puedes ir directamente a su pagina https://colab.research.google.com/ o abrir Google Drive, clickear en el botón “+ Nuevo” y desde ahí elegir la opción “Mas” y clickear en Colaboratory 

Con esto tendrás un notebook de Google Colab a tu disposición!

Un notebook se compone de celdas de codigo y de texto. Una celda de codigo es ejecutable tecleando “Control + Enter”. Para probar que todo esta ok puedes ejecutar el siguiente codigo:

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import sklearn
```

Veras arriba a la derecha que colab se esta conectando a una instancia de computo en la nube (esto colab lo hace solo, no te preocupes!). Esta conexión la realiza solo la primera vez.

Una vez conectado, el código que ingresaste se ejecutara, y veras que efectivamente los imports se harán sin ningún problema por lo que ya tienes todo lo que necesitas para trabajar!

Un solo punto adicional que queda por aclarar es que como estas trabajando en la nube no tienes directamente los archivos de la clase a mano para poder leerlos desde el notebook.

Para poder acceder los archivos del curso puedes hacer lo siguiente:

1. Encuentra el link hacia el archivo que quieres cargar en el repositorio de github https://github.com/JuanPabloMF/datasets-platzi-course
2. Con el link del archivo csv puedes llamar la función de pandas read_csv de la siguiente manera:

```python
import pandas as pd

pd.read_csv('https://github.com/JuanPabloMF/datasets-platzi-course/blob/master/datasets/peliculas.csv?raw=true')
```

**Ya puedes entrar de llenos al curso y empezar a implementar tus primeros modelos de machine learning!**