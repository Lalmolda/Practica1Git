#Aquí escribiré las respuestas de la pŕactica 1 y 2

Preguntas:

*¿Qué comando utilizaste en el paso 11? ¿Por qué?* 

Utilize el comando git reset --hard HEAD~1. Lo utilicé porque el 
enunciado especifica que hay que perder los cambios de nuestro working 
copy, y quería hacerlo con un comando en vez de dos, soy vago!

*¿Qué comandos utilizaste en el paso 12? ¿Por qué?*

Utilizé primero git -reflog para poder acceder al identificador del 
commit donde hice cambios al archivo git-nuestro.md. Después,
Hice un git reset apuntando al identificador del commit. Luego hice 
un git -restore git-nuestro.md, ya que en el working copy estaba 
la versión sin modificar porque hicimos un reset head hard, 
pero en el commit al que nos hemos movido 
estaba el git-nuestro con los cambios de ese commit en el repositorio.
Compruebo con cat git-nuestro.md que, efectivamente, el working copy 
tiene el archivo git-nuestro con los cambios actualizados.

*El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?*

No, no causó ningún conflicto porque está "already up to date", es decir, 
no hay nada que mergear, la rama que quiero absorber ya está absorbida.
He leído que suele pasar cuando es la rama padre de tu rama actual (styled).

*El merge del paso 19, ¿Causó algún confligto? ¿Por qué?*

Sí, causo conflictos porque habia dos ramas que queríamos mergear  
-la recién creada htmlify y styled- con 
contenido diferente en el archivo git-nuestro.md. El conflicto se soluciona haciendo
que tengan el mismo contenido. El merge es non-fast forward.

*El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?*

No, no causó ningún conflicto ya que se resolvieron anteriormente y, al hacer el merge,
master se mueve al último commit, el de styled al hacer el merge non forward con htmlify. 
Sin embargo, hay que tener en cuenta que este ultimo merge si que es fast forward

*¿Qué comando o comandos utilizaste en el paso 25?* 

Utilicé el comando git log --graph

*El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?*

Sí, podría ser fast forward porque master contiene los commit de styled y styled 
contiene a htmlify. A su vez, master es la rama padre de title, y basta con mover master
a title sin crear ningún commit nuevo para poder hacer un merge exitoso.

*¿Qué comando o comandos utilizaste en el paso 27?*

El comando que usé fue git reset HEAD~1

*¿Qué comando o comandos utilizaste en el paso 28?*

Usé el comando git-restore y el nombre del archivo

*¿Qué comando o comandos utilizaste en el paso 29?*

Usé git branch-d title para eliminar la rama title

*¿Qué comando o comandos utilizaste en el paso 30?*

Usé git reflog para saber a qué commit tenía que hacer reset,
y luego git reset --hard < nombre del commit >

*¿Qué comando o comandos utilizaste en el paso 32?*

Utilizo el comando git reset --hard y voy al primer commit del poema,
el commit 6d56cce.

*¿Qué comando o comandos utilizaste en el paso 33?*

Utilizo el comando git reset --hard y voy al ultimo commit donde pusimos
titulo, 74cd8f0
