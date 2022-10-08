## Lista I

 

1. Tendo como dado de entrada a altura (h) de uma pessoa, construa um algoritmo que calcule seu peso ideal, utilizando as seguintes fórmulas: a. Para homens: (72.7*h) - 58 b. Para mulheres: (62.1*h) - 44.7 
 

>A variável **sexo** irá receber como dado digitado pelo usuário “M”, ou “H”. <br> 
> Logo em seguida a variável **h**, irá receber a informação de altura. <br> 
> Ambos os dados serão utilizados posteriormente para fazer os devidos cálculos de peso ideal. <br> 
> <br> 
> <br> 
> Foi utilizado a estrutura **match case** para fazer a verificação do sexo digitado pelo usuário. <br> 
> Dentro de casa case foi utilizada a variável **pesoIdeal** que recebe a fórmula para cálculo de >peso segundo a altura desejada. <br> 
> No final de casa case temos um **print** de saída que informa o peso ideal. 
 
```
sexo = input('Informe (M) para mulher, ou (H) para homem: '); 
h = float(input('informe sua altura: '));` 

match sexo.upper(): 
    case "M": 

        pesoIdeal = (62.1*h) - 44.7; 

        print(f'Seu peso ideal é de {pesoIdeal:.2f}Kg'); 

    case "H": 

        pesoIdeal = (72.7*h) - 58; 

        print(f'Seu peso ideal é de {pesoIdeal:.2f}Kg'); 
  ```
