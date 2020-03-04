# Estruturas de controle de fluxo

Segue a baixo as estrutura de *for*, *while* e *if* do [Octave](http://www.gnu.org/software/octave) junto a estrutura de funcoes.

  * [Estruturas de repeticao](#estruturas-de-repeticao)
    * [For](#for)
    * [While](#while)
  * [Estruturas de fluxo](#estruturas-de-fluxo) 
  * [Funcoes](#funcoes) 
    * [Cost Function](#cost-function)

## Estruturas de repeticao

A seguir esta as estruturas base de *for* e *while*

### For

No geral o *for* pode ser escrito da seguinte meneira, percorrendo ranges:
```
for <range a ser percorrido>,
  // codigo a ser executado 
end;
```

Exemplo pratico:
```
for i=1:10,
  v(i) = 2^i;
end;

// outra forma
indices = 1:10
for i=indices,
  disp(i);
end;
```

### While

O *while* por padrao executa segundo uma condicao verdadeira, como o padrao a seguir:

```
while <condicao>,
  // codigo a ser executado
end;
```
Exemplo pratico

```
i = 1
while i<=5,
  disp(i);
  i = i+1;
end;
```
## Estruturas de fluxo

Os *ifs* no octave nao e tao diferente de outras linguagens, no geral ira seguir o seguinte padrao: 

```
if <condicao>,
  // bloco
elseif <condicao>,
  // bloco
else
  //bloco
end;
```

Exemplo pratico:

```
a = 2;

if a==1,
  disp('A igual um')
elseif a==2,
  disp('A igual dois')
else
  disp(['A igual:', num2str(a)])
end;
```

## Funcoes

Funcoes podem ser declaradas em qualquer arquivo *.m* e acessadas atraves de outros arquivos no mesmo diretorio, porem caso necessario, existe a possibilidade de adicionar outros diretorios atraves do **addpath('<caminho_do_diretorio>')**.

Abaixo segue estrutura base para funcoes no octave
```
function <valor_de_retorno> = <nome_da_funcao>(<argumentos>)

<valor_de_retorno> = <operacao a ser executada>;
```
Exemplo pratico de como seria uma funcao
```
function y = squareThisNumber(x)

y = x^2;
```

### Cost Function

Abaixo segue o exemplo da cost function no octave
```
function J = costFunctionJ(X,y, theta)

m = size(X,1)
predictions = X*theta;
sqrErrors = (predictions-y).^2;

J = 1/(2*m) * sum(sqrErrors);
```