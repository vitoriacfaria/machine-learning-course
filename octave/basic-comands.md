# Comandos basicos do Octave
Segue comandos basicos do [Octave](http://www.gnu.org/software/octave) para execucao dos exercicios.
  * [Operacoes matematicas basicas](#operacoes-matematicas-basicas)
  * [Operadores logicos](#operadores-logicos)
  * [Atribuicoes de variaveis](#atribuicoes-de-variaveis)
  * [Exibicao de variaveis](#exibicao-de-variaveis)
  * [Matrizes e vetores](#matrizes-e-vetores)
    * [Geracao de matrizes e vetores](#geracao-de-matrizes-e-vetores)

## Comandos basicos de operacao

### Operacoes matematicas basicas

Adicao
```
5+6 // ans = 11
```

Subtracao
```
3-2 // ans = 1
```

Multiplicacao
```
5*8 // ans = 40
```

Divisao
```
1/2 // ans = 0.50000
```

Exponenciacao
```
2^6 // ans = 64
```

### Operadores logicos

Igualdade

```
1 == 2 // ans = 0 - false
```

Diferenca
```
1 ~= 2 // ans = 1 - true
```

AND
```
1 && 0 // ans = 0 - false
```

OR
```
1 || 0 // ans = 1 - true
```

XOR
```
xor(1,0) // ans = 1 - true
```

### Atribuicoes de variaveis
 
Formato padrao
```
a = 3;
b = 'hi';
```

Formato abreviado
```
a=3
```

### Exibicao de variaveis
Considere que a = pi, em uma chamada normal de variavel. 
```
a // a = 3.1416
```

Fazendo o display de a
```
disp(a); // 3.1416
```

Display custom
```
disp(sprintf('%0.2f',a)) // 3.14
```
Formato longo
```
format long
a 
// a =  3.14159265358979
```

Formato curto
```
format short
a 
// a =  3.1416
```
### Matrizes e vetores

Atribuicao de vetores
```
V = [1 2 3 4]; // V = 1 2 3 4
```

Atribuicao de matrizes
```
A = [1 2; 3 4]; 
// A = 
      1 2 
      3 4
```
#### Geracao de matrizes e vetores

Vetor atraves de range
```
V = 1:6
// V =
  1 2 3 4 5 6
```

Matriz de 1
```
ones(2,3)
// ans = 
  1 1 1
  1 1 1
```

Matriz de 0
```
zeros(2,3)
// ans = 
  0 0 0
  0 0 0
```

Matriz identidade
```
eye(3)
// ans = 
  1 0 0
  0 1 0
  0 0 1
```
