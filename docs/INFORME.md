1. ¿Por qué el segundo push del apartado 2.2 fue rechazado? ¿Qué dos operaciones hace `git pull` por debajo?

2. En vuestro historial, señalad un merge *fast-forward* y un *merge commit*. ¿Qué los diferencia?

3. ¿Por qué rellenar filas distintas de la tabla no dio conflicto y cambiar `Última revisión` sí?

4. Pegad el mensaje de error del push a `main` protegida y explicad qué regla lo ha bloqueado.
"Enumerating objects: 7, done. Counting objects: 100% (7/7), done. Delta compression using up to 8 threads Compressing objects: 100% (3/3), done. Writing objects: 100% (4/4), 330 bytes | 165.00 KiB/s, done. Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0) remote: Resolving deltas: 100% (2/2), completed with 2 local objects. remote: error: GH013: Repository rule violations found for refs/heads/main. remote: Review all repository rules at https://github.com/grupo01-5023/proyecto02/rules?ref=refs%2Fheads%2Fmain remote: remote: - Changes must be made through a pull request. remote: To github.com:grupo01-5023/proyecto02.git ! [remote rejected] main -> main (push declined due to repository rule violations) error: failed to push some refs to 'github.com:grupo01-5023/proyecto02.git'"

El código de error GH013 en Git indica que nuestro envío fue rechazado debido a infracciones de las reglas del repositorio.

5. ¿Qué comando sacó `.env` del control de versiones sin borrarlo? ¿Por qué la contraseña sigue siendo un problema y qué haríais en un proyecto real? (Pista: la respuesta empieza por lo que hay que hacer con la contraseña, no con el historial.)
El comando fue git rm --cached .env. Quita el archivo de Git pero lo deja en el disco. El problema es que la contraseña sigue en los commits anteriores, así que cualquiera puede verla mirando el historial. En un proyecto real, lo primero sería cambiar la contraseña ya (asumir que está quemada), y luego limpiar el historial con filter-repo o BFG.

6. ¿Qué hace mejor GitHub Desktop que la terminal, y qué no puede hacer? ¿Con cuál habéis entendido mejor el conflicto?
GitHub Desktop es más cómodo para ver los cambios y resolver conflictos visualmente de lado a lado. La terminal hace falta para cosas más avanzadas que el Desktop no cubre bien. El conflicto se entiende mejor a la primera con Desktop, porque lo ves claro.

7. Roles: ¿qué puede hacer un Maintain que no pueda un Write? ¿Quién podría haber quitado la protección de `main`?

8. Si mañana un miembro sube un force push a `main`, ¿qué se pierde y qué lo impide en vuestro repositorio?

9. En la Fase 1 compartíais un portátil y en la Fase 2 cada uno tenía el suyo. ¿Qué diferencia práctica tiene eso para la identidad del autor de cada commit y para cómo aparecen los conflictos?
