# Comandos de manipulacao de dadoss
Segue comandos para a manipulacao de dados e arquivos no [Octave](http://www.gnu.org/software/octave).
  * [Manipulando matrizes e vetores](#manipulando-matrizes-e-vetores)
    * [Uniao de matrizes](#uniao-de-matrizes)
  * [Comandos para arquivos](#comandos-para-arquivos)

## Manipulando matrizes e vetores

Considere as seguintes variaveis
```
A = [
  1 2;
  3 4;
  5 6
]

B = [
  11 12;
  13 14;
  15 16;
]
```

Verificando tamanhos
```
sz = size(A)
// sz = 
      3 2
length(sz)
// ans = 2
```

Selecao de linha da matriz
```
 A(2,:) 
 // ans = 
        3 4
```

Selecao de coluna da matriz
```
 A(:, 2) 
 // ans = 
        2
        4
        6
```

Adicao de colunas na matriz
```
A = [A, [100; 101; 102]]
// A = 
  1 2 100
  3 4 101
  5 6 102
```
Transformar a matriz em vetor
```
A(:)
// ans = 
        1
        3
        5
        2
        4
        6
        100
        101
        102
```
### Uniao de matrizes

Considere o valor inicial das matrizes A e B.

Juncao de A e B em colunas.
```
[A B]
// ans
  1 2 11 12
  3 4 13 14
  5 6 15 16
```

Juncao de A e B em linhas
```
[A; B]
// asn =
  1 2
  3 4
  5 6
  11 12
  13 14
  15 16
```

## Comandos para arquivos

Comando para pasta de arquivos
```
pwd
// no linux
  ans = /home/<user>/<caminho>
```

Carregar arquivo
```
load('<nome o arquivo>.<extensao>')
```

Criar e salvar arquivos
```
save <nome>.mat <dados>;
```

Verificar variaveis declaradas do sistema
```
who 
// A B sz
```

```
whos
//
Variables in the current scope:

   Attr Name      Size        Bytes  Class
   ==== ====      ====        =====  =====
        A         3x2            48  double
        B         3x2            48  double
        ans       1x68           68  char
        sz        1x2            16  double
```