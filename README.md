## Lista I

 

1. Tendo como dado de entrada a altura (h) de uma pessoa, construa um algoritmo que calcule seu peso ideal, utilizando as seguintes fórmulas: a. Para homens: (72.7*h) - 58 b. Para mulheres: (62.1*h) - 44.7 <br>
 
### Documentação
> A variável **sexo** irá receber como dado digitado pelo usuário “M”, ou “H”. <br> 
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

### Documentação 
<br>
> Foram criadas duas variáveis iniciais, uma para conter valor de peso máximo, e outra para conter o. <br>
> valor da multa a ser aplicada no caso de excesso. <br> 
> A variável **peso** irá receber a quantidade em Kg da pesca inserido pelo usuário. <br> 
> <br>
> <br> 
> Para esse caso de uso, foi utilizado uma estrutura condicional **If** , que irá verificar o dado da. <br> 
> variável peso, e da variável peso máximo. Verificando se o valor fornecido pelo usuário é maior. <br> 
> ou menor que o que o permitido.  
> Se o valor for maior que o permitido a variável **multa** irá receber o cálculo do valor da multa.<br> 
> Em ambos os casos teremos um print de saída informando se houve multa ou se está dentro do permitido. <br> 

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

<br><br>
6. Faça um programa que peça o tamanho de um arquivo para download (em MB) e a velocidade de um link de Internet (em Mbps), calcule e informe o tempo aproximado de download do arquivo usando este link (em minutos). 

## Documentação 
<br>
> A variável “tamanhoArquivo” irá receber o o tamanho informado pelo usurário em MB. <br> 
> Logo em seguida a mesma variável irá receber ela mesma, porém com seu valor recebido em <br> 
> MB convertiado para Mbps. <br> 
> <br>
> A variável velocidade irá receber a velocidade da internet a ser informada pelo usuário em Mbps. <br> 
> Após todas as variáveis terem recebido seu respectivos valores, a variável “tempoDownload”, irá <br> 
> <br>
> receber o cálculo que será feito utilizando a variável de tamanho do arquivo, dividida pela velocidade informada. <br> 
> Depois que a variável “tempoDownload” receber o seu devido valor, esse valor será utilizado para fazer a conversando para minutos a ser na variável “minutos”, que em seguida será utilizada para um print que irá mostrar a informação solicitada. 

``` 
tamanhoArquivo = float(input('Quantos MB possui o seu arquivo? ')); 
tamanhoArquivo = tamanhoArquivo * 8; 

velocidade = int(input('Quantos Mbps de velocidade sua internet possui? ')); 

tempoDownload = tamanhoArquivo / velocidade; 

minutos = float(tempoDownload/60); 

print(f'O tempo aproximado de download para esse arquivo será de {minutos:.2f} minutos.'); 

```

## Lista II

2. Faça um Programa que peça um número inteiro e determine se ele é par ou ímpar. 


### Documentação 
<br> 
> A variável “numero” será utilizada para receber o valor infromado pelo usuário que será verificado<br> 
> Logo em seguida foi utilizado uma condição para fazer a verificação, onde irá verificar se o número salvo na variável numero possui resto zero, se for dividido por dois. Caso possua<br> 
> obteremos como resposta uma mensagem informando que o valor é par.<br> 
> Caso a primeira condição não venha ser atendida, o script pulará para a segunda e informará que o número não é impar. 

```  
numero = int(input('Informe o número desejado: '));  

if numero % 2 == 0: 
    print(f'{numero} é um número par') 
else: 
    print(f'{numero} é um número impar')  

```

4. Faça um Programa que peça a idade e a altura de 5 pessoas, armazene cada informação no seu respectivo índice. Imprima a idade e a altura na ordem inversa a ordem lida.  

### Documentação 
<br> 
> Para essa tarefa foram criadas duas listas, uma para conter a altura, e a outra a idade. <br> 
> Também foi utilizado um contador, com a variável “I”.<br> 
> Para que possamos pedir a quantidade de índices a serem inseridos, foi utilizada a estrutura de repetição while. <br> 
> Dentro dessa estrutura, cada uma das estruturas receberá uma função “append()”, para que a cada interação os valores digitados pelo usuário possa ser inserido nas listas.  <br> 
> No print de saída foi utilizada a função “reversed()” que recebeu cada uma das nossas listas e fez com que seus dados fossem mostrados exatamente na ordem inversa a que foram adicionados a lisa. 

``` 
altura = []; 
idade = []; 
i = 1; 

while i <= 5: 

    altura.append(float(input('Informe a altura desejada: '))); 

    idade.append(int(input('Informe a idade desejada: '))); 

    i = i + 1; 
 

print(list(reversed(altura))); 

print(list(reversed(idade))); 

``` 


5. Faça um Programa que leia uma estrutura A com 10 números inteiros, calcule e mostre a soma dos quadrados dos elementos desta estrutura 

### Documentação 
<br> 
> Para essa tarefa foram criadas duas variáveis inicialmente, uma para ser um contador e outra para ser a nossa lista. <br> 
> Também foi utilizado o “while” para poder fazer a nossa repetição, enquanto a condição não fosse atendida. <br> 
> Nessa estrutura de repetição, enquanto a nossa lista não recebesse os 10 número que a preenchesse, o programa irá continuar solicitando o número e adicionando-o a lista. <br> 
> Ainda nessa estrutura nossa lista também irá receber a função “append()” que irá fazer a adição de cada número fornecido pelo usuário, e também receberá como parâmetro a formula necessária para já fazer a adição desses números, com os seus respectivos valores calculados ao quadrado. 
> A cada número adicionado, nosso contador irá receber +1.<br> 
> A variável “soma” recebera a função “sum()”, que receberá como parâmetro nossa lista. Fazendo a soma de todos os valores inseridos nessa lista.<br> 
> A soma desses números é mostrada ao final do programa, em um print de saída. 

``` 

i = 1; 
a = [];  
 

print('Informe 10 números inteiros'); 

while i <= 10: 
    a.append(int(input(f'{i}° número: ')) ** 2); 
    i = i+1; 
 
soma = sum(a); 

print(f'A soma dos quadrados dos elementos adicionados a estrutura é: {soma}') 

``` 
 
 
