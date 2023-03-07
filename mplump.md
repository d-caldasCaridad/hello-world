## Un nuevo comienzo para empezar con el pie derecho después de hacer las cosas mal.

Mucha gente coincide en que la rama ‘main’ debe de mantenerse impecable y como nuevo que soy en este asunto del código, volteo a ver y me doy cuenta de que tengo unos archivos vergonzosamente aceptables después de centenas de **commits**.

Entonces **mi propósito en cuestión de código para este año es**: _**trabajar desde ramas alternas y fusionar desde ‘main’ cuando este listo y presentable el trabajito**…_

`Entonces al iniciar un proyecto, la raíz de este debe de estar limpia. OK.`

* * *

> _Así que estamos en la consola y empezamos a trabajar…_

```
user@computer~$ mkdir new-Project

user@computer~$ cd new-Project

user@computer/new-Project~$ git init
Initialized empty Git repository in/home/user/new-Project/.git/

user@computer/new-Project~$ echo"# new-Project" >> README.md

user@computer/new-Project~$ git add README.md

user@computer/new-Project~$ git commit -m "first commit"
[master 65fe2b4] firts commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

user@computer/new-Project~$ git branch -M main

user@computer/new-Project~$ git checkout -b head
Switched to a new branch 'head'

user@computer/new-Project~$ 

```

Y ahora si estamos listos para trabajar manteniendo la ‘main’ limpia; de esta forma evitamos hacer en un proyecto espantoso, el famoso `git reset --hard` .

Pero ¿ya qué? A nadie le gusta ser el hazmerreir, así que `git reset --hard` puede ser la última mala practica del paseo y olvidar el pasado.

* * *

PARA RESTABLECER COMPROMISO DURO

*   `git reset --hard`
    Establezca el encabezado de rama actual (`HEAD`) en , modificando opcionalmente el índice y el árbol de trabajo para que coincidan. El o por defecto es HEAD en todas las formas.

*   `git reset [mode] [commit]`
    Esta línea de comando restablece el encabezado de la rama actual a y posiblemente actualiza el índice (restableciéndolo al árbol de ) y el árbol de trabajo dependiendo del “mode”. Si se omite “mode”, el valor predeterminado es `--mixed`. Este “mode” puede ser:

*   `--hard`
    Este “mode” restablece el índice y el árbol de trabajo. Cualquier cambio en los archivos rastreados en el árbol de trabajo desde son descartados. Cualquier archivo o directorio sin seguimiento en la forma de escribir cualquier archivo rastreado simplemente se elimina.

DESHACER COMPROMISO PERMANENTEMENTE
Las últimas tres confirmaciones (`HEAD`, `HEAD` y `HEAD~2`) fueron malas y no querrás volver a verlas nunca más. No hagas esto si ya le has dado estos compromisos a otra persona. (Consulte la sección “RECUPERACIÓN DESDE UPSTREAM REBASE” en [git-rebase[1]](https://git-scm.com/docs/git-rebase) para conocer las implicaciones de hacerlo).

PARA DESPUÉS DE DESHACER COMPROMISOS

*   `git-rebase` - Vuelva a aplicar confirmaciones encima de otra sugerencia base.

Si se especifica `<branch></branch>`, `git rebase` realizará un `git switch <branch></branch>`automático antes de hacer cualquier otra cosa. De lo contrario, permanece en la rama actual.

* * *

### Suficiente de teoria. Es hora de ir a la mala practica.

Primero que nada vamos a conservar el trabajo que hemos hecho hasta el momento que a pesar de todo nos costó hacerlo. Así que, **creamos una copia de seguridad**. En esta tenemos el proyecto a salvo y la podríamos llamar “save”.

Ahora si. En ‘main’ invocaremos al demonio con el poder de la “anti-materia” `git reset --hard` . Entonces deberíamos de quedar en nuestro “first commit”.

Luego mover los archivos actuales desde la copia de seguridad a nuestro proyecto (`mv ../save/files .`) para después añadirlos y comprometerlos. Entonces de esta forma solo tedrémos dos commits.

**P.D.** Existe otra forma aun más descerebrada que hasta es vergonzosa si de usar `git reset --hard` se trata. Y consiste en tener todos los archivos abiertos en el IDE para que cuando estemos en nuestro “first commit” los guardemos, agreguemos y comprometamos de nuevo. Ya sabes… `git add .` y `git commit -m ""`.
**NOTA**: es mejor usar una copia de seguridad…

> Si el objetivo es tener el ‘main’ claramente limpio. Tenemos otra forma…

*   hacemos **copia de seguridad**. En esta tenemos el proyecto a salvo y la podríamos llamar “save”.
*   a nuestro proyecto le quitamos el archivo oculto `.git`, ya sabes, con `rm -rf .git` y ahora se han ido los commits.
*   luego empezamos de nuevo con lo mismo de siempre

`echo ## "..." >> README.md` + `git init` + `git add README.md` + `git commit -m "first commit"` + `git branch -M main` + `git remote add origin git@github.com:user/repo.git` + `git push -u origin main` + `git checkout -b head` y `mv ../save/files .` para obtener los archivos desde nuestra copia de seguridad…

* * *

* * *

*   P.D. **Esta es la peor practica cuando hemos hecho el trabajo con otras personas.**
    Antes de hacer algo como esto, debemos de asegurarnos de tener el permiso de la gente involucrada, debemos de tener la seguridad de que nos va a dejar borrar sus memorias (commits), su esfuerzo y buenas intenciones.

*   P.D.D: descargos de responsabilidad… _la personita que se ponga a inventar con lo que dice este tutorial, ya verá. A mi me importa 5 pesos. Y en ningún momento he querido dar consejos de inversión ni finacieros. Aquí cada quién se las arregla como puede…_

* * *

### Otros enlaces recomendados

*   [De Windows a Linux en un Santiamén](https://platzi.com/tutoriales/2292-terminal/19881-de-windows-a-linux-en-un-santiamen/)
*   [La mejor forma de crackear un sistema operativo Linux](https://platzi.com/tutoriales/2292-terminal/21040-la-mejor-forma-de-crackear-un-sistema-operativo-linux/)
*   [Un grave error que debemos evitar al trabajar en WSL](https://platzi.com/tutoriales/2292-terminal/22069-el-error-que-debes-evitar-al-trabajar-con-wsl/)

¡la bendición!

* * *