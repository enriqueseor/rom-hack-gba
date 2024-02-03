## EJECUTAR .EXE EN LINUX CON WINE

Practicamente todas las herramientas para modificar ROMs de Pokemon están formato portable .exe, nativo para Windows OS, no siendo posible ejecutar-lo de forma nativa en Linux.
La solución es instalar-se un programa como Wine(https://wiki.winehq.org/Main_Page) que permite ejecutar los ejecutables de Windows.
El proceso de instalación es muy sencillo, está explicado en su web y es distinto para cada distribución de Linux, por lo que no lo explicaré aquí

## PROBLEMAS EJECUTANDO CON WINE

Al abrir algunos .exe como Advance text o XSE no se ejecutaban. Si lanzamos el comando:
wine Advance-Text.exe
En la ruta del archivo nos arrojará el siguiente error:
0024:err:module:import_dll Library MSVBVM60.DLL
Es un error importando una librería de Visual Basic. La debemos instalar.
Para ello usaremos un programa llamado Winetricks (https://wiki.winehq.org/Winetricks) en donde teneis explicado el proceso de instalación.
Para ejecutar el programa debeis ejecutar en la terminal:
winetricks
Se os abrirá una ventana así:

![](wine-wineprefix.png)
Seleccionamos “Select the default wineprefix”

![](wine-windowsDLL.png)
Ahora lo que queremos hacer es instalar una librería DLL, así que seleccionamos “_Install a Windows DLL or component_” y aceptar.

![](wine-vb6run.png)

Buscamos el Package vb6run y aceptamos.

Nos saldrán estos dos errores, no sufráis y le dais a aceptar.

![](wine-VBlicense.png)
Por último aceptamos los términos de la licencia. Ahora ya podemos ejecutar sin problemas tanto XSE como Advance text.
