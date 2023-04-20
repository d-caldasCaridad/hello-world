# REFLOG OR LOG

Ayer trabajé toda la tarde y cuando quise fusionar mi trabajo con la rama principal, me distraje con el `pull` porque este me trajo mucho trabajo que me puse a revisar.

Cuando terminé de revisar el `pull` que había hecho en esta rama principal, eliminé como es costumbre la rama alterna con la que estaba trabajando y en ese momento recordé que aun **NO** había fusionado el trabajo en el que pasé toda la tarde.

 > Estaba cansado de tanto trabajo y fue como si no hubiera hecho nada. Una desgracia...

Entonces investigué y encontré el comando `git reflog`. Este comando trae una lista de cada `commit`, de cualquier rama que haya habido.

Solo tuve que elegir el SHA debido de la lista que arrojó `git reflog` y luego crear una nueva rama que incluso llamé `new-branch`.
