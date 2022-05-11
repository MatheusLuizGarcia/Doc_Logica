# Decisões e Condições

## Definição
---
**Condição** ->impõe uma  ou mais regras

**Decisão** ->baseado na condição, segue um caminho possível

---
### Desvio condicional simples:

````Se, Então, Fim-se````

Um desvio condicional simples tem por objetivo tomar uma decisão de acordo com o resultado de uma condição, e então executar um bloco de códigos que irá depender do resultado dessa condição.

```
        |
       /\
false /  \   true
-----<cond>----  
|     \  /     |
|      \/    __|___
|           |code  |
|       __  |true__|
|______|__|_____|
        |
```
---
### Desvio condicional composto:

````Se, Então, Senão, Fim-se````

Um desvio condicional composto, como o de simples, executa blocos de código dependendo do resultado da condição, porém também executa blocos de código caso o resultado da condição for falso.

```
           |
          /\
   false /  \   true
   -----<cond>----  
   |     \  /     |
 __|__    \/    __|___
|code |        |code  |
|false|    __  |true__|
   |______|__|_____|
           |
```
---
### Desvio condicional encadeado:

Um desvio condicional encadeado consiste de várias condições em sequência que dependem do resultado da condição prévia e executam códigos diferentes para cada resultado condicional.


```
           |
          /\
   false /  \   true
   -----<cond>----  
   |     \  /     |
 __|__    \/      |
|code |           /\
|false|  false___/  \___true
  |          |   \  /   |
  |         _|_   \/   _|_
  |        |___|   _  |___|
  |          |____|_|___|
  |       __       |
  |______|__|______|
           |
```

### Exercício demonstrativo:

elaborar um algoritmo que efetue o calculo do salario de um funcionario. Considere:
O funcionario deve receber um reajuste de 15% caso seu salario seja menor que $1500.
Caso seja maior que $1500, mas menor que $2500, o reajuste será de 10%, sendo maior, aplique 5%
````
inicio
  |nome : literal
  |sal, salAjuste : real
  |leia "Nome do funcionário:", nome
  |leia "Salário do funcionário:", sal
  |se sal>=1500
  |  |se sal>=2500
  |  |  |calcule salAjuste=sal*1,05
  |  |senão calcule salAjuste=sal*1,1
  |  |fim-se
  |senão calcule salAjuste=sal*1,15
  |fim-se
  |escreva "Nome: ",nome,""
  |escreva "Salário reajustado: ",salAjuste,""
fim
````
---
### Estruturas de controle (laços de repetição):

````Enquanto, Faça, Fim-enquanto````

Consiste de usar o código enquanto para repetir uma ação até uma condição ser verdadeira.

```
           |
          /\
   false /  \   true
   -----<cond>----  
   |     \  /     |
 __|__    \/    __|___
|code |____^   |code  |
|false|        |true__|
                  |
                  |
```

### Exercício demonstrativo:

1 - Criar uma variável para servir de contador com valor inicial 1;

2 - Enquanto o valor do contador for <=5, processar os passos 3,4,5,6;

3 - Ler um valor para a variável x;

4 - Efetuar o produto de x por 3 e implicar ao valor R;

5 - Apresentar o valor R na tela;

6 - Acrescentar o valor 1 ao contador;

7 - Quando o contador for >5 encerre o processo.

````
inicio
  |x, R, con : real
  |con = 1
  |enquanto con<=5 faça
  | |leia "Insira um valor para x", x
  | |R = x * 3
  | |escreva "valor de R = ",R,""
  | |con = con + 1
  |fim-enquanto
fim  
````
