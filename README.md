PRACTICA DCA

Alias locales creados:
co = checkout
ci = commit
st = status
br = branch
ejemplo: "git config alias.co checkout"

Crear alias globales:
ejemplo: “git config —-global alias.co checkout”

Encontrar fallos (git bisect):
- primero commit: añado readme
- segundo commit: añado codigo
- tercer commit: fallo en el codigo
- cuarto commit: añado nombre en el codigo
- quinto commit: añado footer con el correo electronico

Comienzo la a utilizar git bisect para encontrar el fallo

- Marco el quinto commit como malo (git bisect bad)
- Indico que commit esta sin fallos (git bisect good 3f0daa895d05e04ff043f569c21480340d0450b7)
- Voy indicando que commit estan bien o estan mal segun indica git

Resultado:

d614ba36354f4a41e3fefe2798b15bd62657b342 is the first bad commit
commit d614ba36354f4a41e3fefe2798b15bd62657b342
Author: Alberto Martinez <albertoml.ohara@gmail.com>
Date:   Thu Dec 11 18:16:33 2014 +0100

fallo en el codigo, div sin cerrar

:100644 100644 77171041bc8e1d212f1de95cc381f74b0be5aed9 b33ae425131602d38e34282ea7fdc0afdb044c46 M	practica.html
MacBook-Air-de-Alberto:practica10Git Alberto$ 

Hooks:
renombrado archivo pre-push.sample a pre-push
-- Este hook prohibe hacer push commits que comiencen por WIP
-- Hacemos un commit cuyo mensaje es "WIP hooks prueba"
-- Resultado del hook:
MacBook-Air-de-Alberto:practica10Git Alberto$ git push origin master
Found WIP commit in refs/heads/master, not pushing
error: failed to push some refs to 'git@github.com:albertoml/dca.git'
MacBook-Air-de-Alberto:practica10Git Alberto$ 



