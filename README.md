## Lista I

 

1. Tendo como dado de entrada a altura (h) de uma pessoa, construa um algoritmo que calcule seu peso ideal, utilizando as seguintes fórmulas: a. Para homens: (72.7*h) - 58 b. Para mulheres: (62.1*h) - 44.7 <br>
 
### Documentação
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
<br>
<br>

2. João Papo-de-Pescador, homem de bem, comprou um microcomputador para controlar o rendimento diário de seu trabalho. Toda vez que ele traz um peso de peixes maior que o estabelecido pelo regulamento de pesca do estado de São Paulo (50 quilos) deve pagar uma multa de R$ 4,00 por quilo excedente. João precisa que você faça um programa que leia a variável peso (peso de peixes) e calcule o excesso. Gravar na variável excesso a quantidade de quilos além do limite e na variável multa o valor da multa que João deverá pagar. Imprima os dados do programa com as mensagens adequadas. 

 

>### Documentação 
><br>
>Foram criadas duas variáveis iniciais, uma para conter valor de peso máximo, e outra para conter o <br>
>valor da multa a ser aplicada no caso de excesso. <br> 
>A variável **peso** irá receber a quantidade em Kg da pesca inserido pelo usuário. <br> 
><br>
><br> 
>Para esse caso de uso, foi utilizado uma estrutura condicional **If** , que irá verificar o dado da <br> variável peso, e da variável peso máximo. Verificando se o valor fornecido pelo usuário é maior <br> ou menor que o que o permitido.  
>Se o valor for maior que o permitido a variável **multa** irá receber o cálculo do valor da multa.<br> 
>Em ambos os casos teremos um print de saída informando se houve multa ou se está dentro do permitido. <br> 

``` 
pesoMax = 50; 

valorMulta = 4; 
 

peso = float(input('Informe quantos kg pescou: ')); 
 

if peso > pesoMax: 

    excesso = peso - pesoMax; 

    multa = excesso * valorMulta; 

    print(f'Você pescou {excesso}Kg além do permitido. \n Deverá pagar uma multa no valor de R${multa:.2f}'); 

elif peso <= pesoMax: 

    print(f'Parabéns, você pescou {peso:.2f}Kg e não precisará pagar multa.'); 

``` 
 
