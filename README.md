# tallerVideojuegos

## Comandos
- install_games -> crea la carpeta games que incluyen games
  - cd games -> load jelpi -> run #esto ejecutara la demo y con esc podemos salir de la ejecucion
- install_demos -> crea la carpeta demos que incluyen demos
  - cd demos -> load jelpi -> run #esto ejecutara la demo y con esc podemos salir de la ejecucion
- help -> para ayuda
ambos crean
## Comandos conocidos
- cd, ls, mkdir, cls, ctrl + l para limpiar la consola, print("Hola mundo!")
- reboot para reiniciar la consola

## Crear un pequeño script
- Con esc cambiamos al modo editor, en las pestañas superiores, primero encontramos el editor de texto, luego el de sprites, editor de mapas, editor de soundfx y un tracker para la musica

  ```lua
  print("Hola mundo!")
  ```
- luego esc nuevamente para volver al cli
- para guardar basta con escribir save [nombre del archivo] y quedara guardado en nuestro directorio actual con la extension .p8, una vez ya guardado para actualizar el guardado ctrl + s
- Cargar programa: load [nombre programa sin .p8]
- run o ctrl + r

# Sintaxis
  - aqui existe el ```and``` y el ```or```
  ## Operaciones logicas
  ```lua
  vidas = 10
  ataque = 40
  -- puede_entrar = vidas > 8 and ataque > 20 --esto retorna true o false dependiendo de los valores
  -- puede_entrar = vidas > 9 or ataque > 20 --esto retorna true o false dependiendo de los valores
  print(puede_entrar)
  ```

## bucles
### while
  ```lua
  --while normal
  x = 0
  while (x<10) do
    x=x+1
  end
  --while true
  while(true) do
    x=x+1
    print(x)
  end
  ```
  ### For
  ```lua
  x=0
  for i=0,9 do
    x+=1
    print(x)
  end
  -- for con vars
  inicio = 0
  fin = 9
  for i=inicio, fin do
    x+=1
    print(x)
  end
  ```

## Funciones
  - La funcion _update se ejecuta 30 veces por segundo
   ```lua
    function _update()
      print("hola mundo")
    end

  function print10()
    x=0
    for i=0,9 do
      x+=1
      print(x)
    end
  end
  print10()
  -- funcion con parametros, variables de scope local deben ser definidas anteponiendo la palabra local
  function print10(low, high)
    local x = low
    for i=low, high do
      print(x)
      x+=1
    end
  end
  print10(0, 9)
   ```
## Estructuras de control
  ```lua
-- IF
  x=10
  y=20
  if x > y then
    print("x es mayor que y")
  elseif x<y then
    print("x es menor que y")
  else
    print("x es igual que y")
  end

-- if
  tipo = "fuego"
  dmg = 40
  mdmg = 20
  if tipo == "pelea" then
    dmg+=10
  elseif tipo=="fuego" then
    mdmg+=10
  end
print("tipo: "..tipo)
print("dmg: "..dmg)
print("mdmg: "..mdmg)
