# 5.-Piano-de-papel


# Objetivos
•	Crear un piano utilizando componentes electrónicos con la finalidad que sea usado por el público general.

•	Diseñar un piano a menor escala que sea capaz de emitir el mismo sonido que un piano real.

•	Simular un piano aplicando conceptos de electrónica y sistemas embebidos reduciendo costos con la finalidad de que el público general entone sus notas musicales en el piano electrónico.

# Descripcion del proyecto

Como proyecto se ha realizado un piano en base a componentes electrónicos, el cual tiene como finalidad tocar ciertas canciones en base a sus letras musicales. Se ha representado las notas musicales mediante pulsadores, sin embargo, se ha implementado con ciertas notas musicales, las cuales son Do, Re, Mi, Fa, Sol, La, Si. Por otra parte, se agregó un pulsador extra, el cual al ser presionado se emitirá una canción determinada. Por último, se agregó una pantalla Lcd, el cual, por pantalla se vere las notas musicales presionadas e incluso el titulo y el autor de la canción que por defecto se activa al presionar el pulsador extra.

# Lista de materiales
![image](https://user-images.githubusercontent.com/110777989/189981873-c3e43a69-c8ba-491d-89b0-31b08db55f4e.png)
![image](https://user-images.githubusercontent.com/110777989/189982339-ac18100d-793f-4de2-ab9e-3da925f74903.png)

# Explicacion del código del proyecto
![image](https://user-images.githubusercontent.com/110777989/189982568-bd9d6d7b-f4ec-4fd3-8ac7-55d970524fa9.png)

Cada nota musical trabaja a una frecuencia dada, por tanto, mediante la función tone de Arduino, nos permite establecer la frecuencia y el tiempo de duración del sonido en milisegundos. Cada nota musical es representada mediante un pulsador.

El sonido por medio del buzzer comenzara a ser escuchado siempre y cuando se haya presionado el pulsador o nota musical, para esta sección se usó la configuración pull up.

Por último, se agregó una pantalla lcd con i2c, para optimizar pines del Arduino, la cual mostrara cada nota musical, acorde a la nota musical tocada por el usuario.
Como extra, se creó una función el cual guarda una canción determinada, y cada nota de la canción tiene su respectiva frecuencia, y al presionar su respectivo pulsador, comenzará a sonar la canción, y mediante la pantalla lcd se podrá observar el título de la canción y su respectivo autor.

El usuario tiene que presionar los pulsadores acordes a la nota musical que desee tocar, y así puede entonar cualquier canción, que este dentro de las notas musicales que se implementó en nuestro piano. Y si no desea entonar ninguna canción, puede presionar el botón para escuchar la canción que se implementó por defecto en el Arduino.

# Posibles Mejoras

•	Agregar un circuito amplificador, para agregarle un sistema como bocina, para que el sonido sea más alto, y pueda más gente escuchar.

•	Agregar más notas musicales, para que se pueden tocar una mayor variedad cantidad de canciones.

•	Mediante un teclado, el usuario eliga que canción le gustaria que el piano entone automaticamente por defecto.

•	Agregar un buzzer pasivo para cada nota musical, de tal manera que al presionar distintas musicales al mismo tiempo, el sonido que emita el piano será rápidamente de ambas notas. Dado que, si se presiona muchas notas musciales al mismo tiempo se distorsiona el sonido del buzzer y el atmega 328p no sabrá que nota mismo sonar.

# Conclusiones
•	Se implementó un piano por medio de componentes electrónicos con la finalidad que muchas personas puedan entonar las notas musicales de su preferencia acorde a sus canciones favoritas, y a su vez funciona como forma de distracción para la gente.

•	Se simuló por medio de una plataforma el funcionamiento de un piano electrónico.

•	Se diseñó un piano a menor escala con componentes electrónicos capaz de entonar el sonido de ciertas notas igual que un piano real.


