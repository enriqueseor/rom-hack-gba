
![](xse.png)
Una de las cosas más importantes del ROM hacking son los scripts. Estos nos permiten construir la histeria de nuestro juego y dependiendo de los conocimientos de scripting que tengamos podremos construir una historia mejor o peor. La herramienta que vamos a utilizar para hacer scripts será eXtreme Script Editor (XSE).

Para abrir los Scripts de la ROM con XSE desde Advance Map tenemos que configurar XSE como editor de scripts. Vamos a “_Settings < Choose script editor_” e indicamos la ruta del ejecutable.

![](choose-script-editor.png)

## CONSTRUYENDO UN SCRIPT BÁSICO: ¡¡¡HOLA MUNDO!!!

Dentro de la pestaña de eventos seleccionamos a una persona y cliqueamos en “O_pen script_”. Si habéis seguido el paso anterior se nos abrirá XSE automáticamente con el script del mini.

![](open-script.png)

El siguiente script seria el ejemplo más básico que hay. Cuando interactuemos con este mini nos dirá “Hola mundo”.

![](hello-world-script.png)

Como podéis ver he comentado el script para que podáis ver que es cada cosa. Para hacer comentaros basta con poner un apostrofe (“**‘**”) y todo el código de esa línea que se encuentre a la derecha el compilador no lo tendrá en cuenta.

Otras aclaraciones:

| #dynamic | indica que el offset del script será de tipo dinámico |
| --------- | ---- |
| 0x800000 | es el offset a partir del que el compilador buscará espacio en la ROM, dándonos después el offset del script que podría ser por ejemplo 800031. |
| msgbox | Indica que ha de abrir una caja de texto |
| @talk | Es el puntero del mensaje, podemos ponerle el nombre que queramos. Va a buscar la frase que tiene el msgbox |
| 0x6 | Es el parámetro que pide el msgbox, y determina el tipo de msgbox que es. Se puede substituir por MSG_NORMAL. |
| #org @talk | Establecemos el puntero del mensaje |
| = | Asignamos el texto del script |

Una vez hayamos acabado hemos de compilar el script. Para ello solo debemos cliquear sobre el botón con dos engranajes que hay en la barra de menú:

![](compiler.png)

Se nos abrirá una pestaña con la salida del compilador.

![](compiler-output.png)

Copiamos el offset que nos a dado en @start en el Script offset de A-Map:

![](offset.png)

Es importante no quitar el símbolo de $, sino no compilara correctamente.

![](hello-world-result.png)

Este sería el resultado.