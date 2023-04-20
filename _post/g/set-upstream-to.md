# Recuperar la rama principal a una rama para trabajar en local

No sé por qué razón perdí mi repositorio en local pero por suerte contaba con él en remoto.

Realmente si existía solo que las últimas actualizaciones se habían perdido. Entonces abrí una rama que llamé local (`git checkout -B local`) e hice un pull (`git pull`)

Entonces tuve conflictos para traer este repo o para hacer `git pull` desde mi rama local a este repositorio remoto.

 > Lo bueno es que Git es bastante instructivo y me enseñó a resolver este problema.

Primero me informó sobre el conflicto y me hizo par de recomendaciones, un par de líneas de comando de las cuales una era para abortar y la otra fue `git branch --set-upstream-to=origin/<branch> <branch>`. Esta última es la opción que escogí, donde la primer `<branch>` es para señalar que rama de tu repositorio remoto quieres y la segunda `<branch>` es para indicar en que rama local quieres traer o hacer `git pull`. Mi rama local se llamaba "local" ¿lo recuerdas? Ya lo había mencionado.

+ Mi línea de comando quedó así:

```sh
d@caldasCaridad:~$ git branch --set-upstream-to=origin/main local
```

Luego de esto la consola me dice que ejecute `git pull git@github.com:d-caldasCaridad/wCsJS.git main` e hice luego de esto el trabajo que tenía para hacer y lo fusioné con mi `main` local para luego hacer `git push`.
