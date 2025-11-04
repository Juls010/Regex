const regex1 = \patrón/flags

const regex2 = new RegExp('patrón', 'flags')


Flags (banderas)

g -> global:  Buscar todas las coincidencias
i -> case sensitive: ignorar mayusculas y minusculas
m -> multiline: ^ y $ funcionan en cad alinea
s -> dotall: el punto (.) incluye saltos de linea
u -> unicode: habilitar soporte completo Unicode
y -> sticky: busca desde la posición exacta


Caracteres especiales

basicos
    . cualquier caracter excepto salto de linea
    /d digito (0-9)
    /D NO digito
    /w caracter alfanumerico (a-z,A-Z,0-9)
    /W NO alfanumerico
    /s espacio en blanco (espacio, tap, salto de linea)
    /S no espacio en blanco

anclas
    ^ inicio de la cadena
    $ fin de cadena
    /b limite de palabra
    /B no limite de palabra

cuantificadores
    * 0 o más veces
    + 1 o más veces
    ? 0 o 1 vez (opcional)
    {n} exactamente n veces
    {n,}  n o mas veces
    {n,m} entre n y m 

grupos y conjuntos
    [abc] cualquiera de a b o c
    [^abc] cualquier caracter excepto a b o c
    [a-z] rango de la a z 
    (abc) grupo de captura
    (?:abc) grupo sin captura
    | OR lógico

metodos de JS
metodos de string
test() verificar si hay coincidencia (retorna boolean)
const regex = /hola/i
regex.test("Hola mundo"); // true

match() retorna array con coincidencia

"2025-11-04".match(/\d+/g)  // ["2025","11","04"]

search() retorna indice de la primera coincidencia
"hola mundo".search(/mundo/) // 5

replace()
split()

metodos del propio regex RexExp
exec() busca coincidencia y retorna informacion detallada

const regex = /(\w+)@(\w+)/;
const resultado = regex.exec("email@dominio.com");

// resultado[0]: coincidencia completa
// resultado[1], resultado[2]: grupos capturados