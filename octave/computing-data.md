# Comandos de computacao de data
Segue comandos de computacao de data do [Octave](http://www.gnu.org/software/octave) para execucao dos exercicios.

## Comandos com matrizes

O programa respeita a multiplicacao de matrizes, por isso certifique que a segunda matriz tenha a quantidade de colunas igual a quantidade de linhas da primeira.
```
A*C // A(2x3) e C(2x2)
```

Para multiplicar pelos elementos espelhos das matrizes(ex A[1, 1] e C[1, 1]) pasta usar a seguinte denotacao:
```
A .* B
A .* 2 // multiplica todos os elementos por 2
A .^ 2 // exponencia todos os elementos por 2
A ./ 2 // divide todos os elementos por 2
```

Outros comandos habilitados para matrizes e vetores:
```
log(A) // logaritmo dos elementos
exp(A) // exponenciacao na base 'e'
abs(A) // modulariza os elementos
```

Matriz transposta
```
A'
```

Procurar elementos na matriz ou vetor usando find lhe retornara as posicoes encontradas.
```
A = [1 5 3 2]
find(A < 3)
// ans = 
    1 4
```

Na matriz o comando **sum()** soma todos os valores de cada coluna e retorna um vetor com os valores enquanto no vetor todos os valores da linha sao somados. Isso ocorre tambem para **prod()** que fara a multiplicacao.

Comandos de aproximacao
```
floor(A) // arredonda valores para um inteiro abaixo
ceil(A) // arredonda valores para um inteiro acima
```

Buscar maior valor
```
max(A(:))
```

Girar matriz
```
flipud(A)
```

Inverter matriz
```
pinv(A)
```