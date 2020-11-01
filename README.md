# Setup del curso

En este curso utilizaremos Jupyter Notebooks y el stack Pydata, que incluye las librerías Numpy, Pandas, Matplotlib y Scikit-learn.

En lo que sigue te presento 3 opciones para trabajar con estas tecnologías:

1. Trabajar en el cloud gracias a la excelente herramienta **Google Colab**.
2. Trabajar en local en tu computadora gracias a **Anaconda**.
3. Trabajar en tu computadora virtualizando a través de contenedores con **Docker**.

**Google Colab es la opción mas facil de usar, así que esta es la opción oficial recomendada por el curso.**

Solo lee las instrucciones para las otras opciones si por alguna razon en particular prefieres ocupar una de ellas (Anaconda permite que trabajes en local, y Docker es bueno para usos en producción).

## Google Colab

Google Colab es muy similar en su uso a Google Docs. Puedes ir directamente a su pagina https://colab.research.google.com/ o abrir Google Drive, clickear en el botón “+ Nuevo” y desde ahí elegir la opción “Mas” y clickear en Colaboratory (como se ve en la imagen)

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

------

## Otras opciones

### Anaconda

Para instalar Anaconda debes:

- Ir a https://www.anaconda.com/distribution/
- Elige tu sistema operativo: Windows/Linux/macOS
- Descarga el **instalador gráfico** para la arquitectura que corresponda a la CPU de tu computadora (32 bits o 64 bits)

Cuando hayas descargado el instalador gráfico y lo hayas abierto se te solicitaran diversas confirmaciones, puedes tomar las opciones por defecto.

Anaconda quedara luego de estos pasos instalado dentro de tus aplicaciones.

Abre Anaconda y en la home tendras Jupyter disponible. Abrelo con botón Launch.

El ambiente por defecto en el que Anaconda te hara trabajar se llama “base (root)” y ya contiene las librerías esenciales de Pydata.

Crea un nuevo notebook de python 3 y estas listo para trabajar!

### Docker

Te recomiendo usar Docker solo si ya tomaste alguno de los cursos de Platzi que te ensenan a usarlo, o si ya tienes experiencia con esta herramienta.

1. Primero instala Docker en tu computador

Ve a https://www.docker.com/products/docker-desktop y haz click en descargar para tu OS.

Dale click a descargar. Esto descargara un archivo (en el caso de windows .exe) que es el instalador y pesa 914 MB.

Abre el archivo instalador que vienes de descargar y sigue las instrucciones de instalación y con esto ya tendrás Docker instalado.

1. Abre la aplicación Docker y dale “start”.
2. En tu Terminal crea la imagen del curso.

***Importante\***: Si trabajas en windows asegúrate de habilitar una terminal de linux en tu computador. Esto es fácil, y lo puedes ver en el curso de prework https://platzi.com/clases/1650-prework/21960-configuracion-de-zsh-para-windows-con-linux-shell/

```bash
mkdir ~/platzi-ml
cd ~/platzi-ml 
git clone https://github.com/JuanPabloMF/arara-docker-stacks.git
cd arara-docker-stacks/ararads-base
sudo docker build -t ararads-base:1.0 .
```

Con estos comandos habrás creado un folder donde trabajar, abras descargado los Dockerfiles provistos por el curso, y creado una imagen de nombres “ararads-base:1.0”.

1. Descargar CSVs y Datasets

```bash
cd ~/platzi-ml 
mkdir vol
cd vol
git clone https://github.com/JuanPabloMF/datasets-platzi-course
```

1. Instanciar contenedor

```bash
sudo docker run -ti --name platzi-ml -v ~/platzi-ml/vol:/home/juanpablo/work/vol -p 8888:8888 ararads-base:1.0 start-notebook.sh --NotebookApp.token=''
```

1. Acceder al Notebook

Abrir en chrome la url http://localhost:8888/ y ya tienes un notebook listo para trabajar! 