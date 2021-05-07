# Setup del curso

En este curso utilizaremos Jupyter Notebooks y el stack Pydata, que incluye las librerías Numpy, Pandas, Matplotlib y Scikit-learn.

En lo que sigue te presento 3 opciones para trabajar con estas tecnologías:

1. Trabajar en el cloud gracias a la excelente herramienta **Google Colab**.
2. Trabajar en local en tu computadora gracias a **Anaconda**.
3. Trabajar en tu computadora virtualizando a través de contenedores con **Docker**.

**Google Colab es la opción mas fácil de usar, así que esta es la opción oficial recomendada por el curso.**

Solo lee las instrucciones para las otras opciones si por alguna razón en particular prefieres ocupar una de ellas (Anaconda permite que trabajes en local, y Docker es bueno para usos en producción).

## Google Colab

Google Colab es muy similar en su uso a Google Docs. Puedes ir directamente a su pagina https://colab.research.google.com/ o abrir Google Drive, clickear en el botón “+ Nuevo” y desde ahí elegir la opción “Mas” y clickear en Colaboratory 

Con esto tendrás un notebook de Google Colab a tu disposición!

Un notebook se compone de celdas de código y de texto. Una celda de codigo es ejecutable tecleando “Control + Enter”. Para probar que todo esta ok puedes ejecutar el siguiente código:

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import sklearn
```

