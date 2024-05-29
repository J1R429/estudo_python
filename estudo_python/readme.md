[SEÇÃO 1: APRESENTAÇÃO](#seção-1:-apresentação)
[SEÇÃO 2: PREPARANDO O AMBIENTE](#seção-2:-preparando-o-ambiente)
[SEÇÃO 3: INTRODUÇÃO Á LINGUAGEM PYTHON](#seção-3:-introdução-á-linguagem-python)
[SEÇÃO 4: VARIÁVEIS E TIPOS DE DADOS EM PYTHON](#seção-4:-variáveis-e-tipos-de-dados-em-python)
[SEÇÃO 5: ESTRUTURAS LÓGICAS E CONDICIONAIS EM PYTHON](#seção-5:-estruturas-lógicas-e-condicionais-em-python)
[SEÇÃO 6: ESTRUTURAS DE REPETIÇÃO EM PYTHON](#seção-6:-estruturas-de-repetição-em-python)
[SEÇÃO 7: COLEÇÕES PYTHON](#seção-7:-coleções-python)
[SEÇÃO 8: FUNÇÕES EM PYTHON](#seção-8:-funções-em-python)
[SEÇÃO 9: COMPREHENSIONS EM PYTHON](#seção-9:-comprehensions-em-python)
[SEÇÃO 10: EXPRESSÕES LAMBDAS E FUNÇÕES INTEGRADAS](#seção-10:-empressões-lambdas-e-funções-integradas)
[SEÇÃO 11: DEBUGANDO E TRATANDO ERROS](#seção-11:-debugando-e-tratando-erros)
[SEÇÃO 12: TRABALHANDO COM MÓDULOS PYTHON](#seção-12:-trabalhando-com-módulos-python)
[SEÇÃO 13: LEITURA E ESCRITA EM ARQUIVOS](#seção-13:-leitura-e-escrita-em-arquivos)
[SEÇÃO 14: ITERADORES E GERADORES PYTHON](#seção-14:-iteradores-e-geradores-python)
[SEÇÃO 15: DECORADORES EM PYTHON](#seção-15:-decoradores-em-python)
[SEÇÃO 16: ORIENTAÇÃO A OBJETOS COM PYTHON](#seção-16:-orientação-a-objetos-com-python)
[SEÇÃO 17: HERANÇA E POLIMORFISMO](#seção-17:-herança-e-polimorfismo)
[SEÇÃO 18: MANIPULANDO ARQUIVOS CSV E JSON](#seção-18:-manipulando-arquivos-csv-e-json)
[SEÇÃO 19: TRABALHANDO COM DATA E HORA EM PYTHON](#seção-19:-trabalhando-com-data-e-hora-em-python)
[SEÇÃO 20: TESTES COM PYTHON](#seção-20:-testes-com-python)
[SEÇÃO 21: GERENCIAMENTO DE MEMÓRIA EM PYTHON](#seção-21:-gerenciamento-de-memória-em-python)
[SEÇÃO 22: CHEGAGEM DE TIPOS EM PYTHON](#seção-22:-chegagem-de-tipos-em-python)
[SEÇÃO 23: NOVIDADES DO PYTHON 3.8](#seção-23:-novidades-do-python-3.8)
[SEÇÃO 24: PROJETO PYTHON 1 - GAME](#seção-24:-projeto-python-1---game)
[SEÇÃO 25: PROJETO PYTHON 2 - MERCADO](#seção-25:-projeto-python-2---mercado)
[SEÇÃO 26: PROJETO PYTHON 3 - BANCO](#seção-26:-projeto-python-3---banco)
[SEÇÃO 27: ENCERRAMENTO](#seção-27:-encerramento)


# SEÇÃO 1: APRESENTAÇÃO
- realizado

# SEÇÃO 2: PREPARANDO O AMBIENTE
- ambiente virtual - 
    - instalação do virtualenv e virtualenvwrapper
    - essas ferramentas permitem criar ambientes isolados de desenvolvimento python, torna possivel a utilização de diversas bibliotecas em um mesmo ambiente sem que haja conflito entre elas
    - ou seja para cada projeto é criado um ambiente apenas para ele

- para criar o ambiente 
    - comando: mkvirtualenv nome_projeto
    - necessário a instalação da biblioteca
        - pip install virtualenv virtualenvwrapper-win 
        - aqui encima tem 2 bibliotecas diferentes sendo instaladas ao mesmo tempo  
    - apos é necessário criar um ambiente novo no sitema do computador
        -  painel de controele >> sistema >> sisitema >> configurações avançadas do sistema >> variaveis de ambiente
        - clicar em novo, nome do ambiente será WORKON_HOME, valor será o caminho C:\Users\jessi\Envs 
    - testa se a variavel é reconhecida, no prompt 
        -  echo %WORKON_HOME%
    - depois de criado pode relizar o comando mkvirtualenv nome_projeto
        - estando ativo, apos criado o nome do ambiente virtual irá aparecer em () no inicio do prompt

- no programa pycharm é possivel salvar os novos projetos no ambiente virtual cirado acima
    - na tela de criar o novo projeto é necessário selecionar o interpretador existente e realizar a sua busca

- para entrar no ambiente 
    - workon nome_ambiente

# SEÇÃO 3: INTRODUÇÃO Á LINGUAGEM PYTHON
- pep8 - qualidade do codigo do python
    - pep - proposta de melhoramento do pyton
    - utilizar camel case para nome de classe
    - utilizar nomes minusculos separados por underline para funções ou variaveis 
    - utilize 4 espaços para identação, não recomendado utilizar o tab
    - separar funções e definições de classe com 2 linhas em branco
    - metodos dentro de uma classe devem ser separadas com uma unica linha em branco
    - import devem ser feitos em linhas separadas
    - sem espaço em expressões e instruções

- o dir e o help
    - são utilitários python para auxiliar na programação
    - dir - apresenta todos os conteudos e funções/metodos disponiveis
    - help - apresenta a documentação


## recebendo dados do usuário
- utilizar o input(em ingles significa entrada)
- todo dado recebdo pelo input é do tipo string
    - sendo necessário em muitos casos sua conversão pelo case
        - int(input('')) 

```python
print('qual o seu nome?')
nome=input()

print ('seja bem vindo %s' % nome)

# a porcentagem s %s pega a variavel mencionada no final e substitui, se tiver mais de uma vriavel mencionada no final neessário colocar entre ()
```
- %s é um marcado de posição que será substituido pelo valor da variavel 

- para deixar tudo maiusculo >> print(nome.upper())
- para deixar tudo minusculo >> print(nome.lower())
- para colocar cada palavra da frase em uma lista de strings >> print(nome.split())
- para pegar determinadas posições >> print(nome[0:4])
- para trocar alguma string >> print(nome.replace('g', 'p'))
- para escrever ao contrário [::-1]


# SEÇÃO 4: VARIÁVEIS E TIPOS DE DADOS EM PYTHON
- string - o que stiver em aspas simple ou duplas ou ainda triplas, utilizada para escrever frases em linhas diferentes

- tipos numericos 
    - inteiro, float
    - o separador das casas decimais é o ponto e não a vírgula
    
- ao inves de utilizar ponto nos numeros grandes é pssivel utilizar _
    - 1.000.000 >> 1_000_000


- a função type() informa qual o tipod e dado colocado entre os ()


```python
num=42

num += 1 # mesma coisa que falar num=num+1
```

- é possivel realizar dupla atribuição, ou seja, declara duas variaveis
```python
valor1, valor2 = 1, 44
```

- BOOLEANO
    - True ou False

- operações basicas
    - negação (not) -
        - fazendo a negação, se o valor booleano for verdadeiro o resultado é falso; se o valor for falso o resultado é verdadeiro
    - ou (or) - um ou outro deve ser verdadeiro para ser verdadeiro
    - e (and) - ambos os valores devem ser iguais

- escopo de variaveis
    - variaveis globais - são reconhecidas, seu escopo compreende todo o programa
    - variaveis locais - são reconhecidas apenas no bloco onde são declaradas
    - declaração da variavel >> nome_variavel = valor_variavel


# SEÇÃO 5: ESTRUTURAS LÓGICAS E CONDICIONAIS EM PYTHON

## if, else, elif
- estrutura condicional - 

```python
idade = 6

if idade < 18:
    print('menor de idade')
elif idade ==18:
    print('tem 18 anos')
else:
    print('maior de idade')
```

## estrutura logicas
- and, or, not, is(é)
    - operadores unários - not, is
        - o is é como se fosse uma pergunta >> ativo =True; print(ativo is False); resultado será False 
    - operadores binários - and, or

```python
ativo= True
logado = True

if ativo and logado:
    print('bem-vindo usuário')
else:
    print ('vc precisa tivar a sua conta')
```


# SEÇÃO 6: ESTRUTURAS DE REPETIÇÃO EM PYTHON
- loops - utilizamops para iterar sobre sequencias ou sobre valores iteraveis
    - for
    - while - 

- exemplos de iteraveis- string, listas, range
    - no range o valor final não é incluido

```python
# exemplo de estrutura

for item in interavel:
    //execução do loop
```

```python
#exemplo de for 1

nome = 'jessica fernandes'
lista = [1, 3, 5, 7, 9]
numeros = range [1, 10]

for letra in nome:
    print(letra)

for numero in lista:
    print(numero)

for numero in range(1, 10 ):
    print(nuemro)
```

- no print se não desejar que pule uma linha, ao final dos () é necessário colocar , end=''
- a string pode ser multiplicada 

```python
nome = 'jessi'
for num in range(1, 11):
    print(f'{nome*num}')
```

- range - utilizados para criar sequencias numericas, não de forma aleatoria mas sim de maneira especifica
- formas gerais
    - range(valor de parada)
    ```python
    for num im range(11):
        print(num)
    ```
    - range(valor_de_inicio, valor_de_parada)
    ```python
    for num in range(1, 11):
        print(num)
    ```
    - range(valor_inicio, valor_parada, passo)
    - neste é possivel decrementar exemplo (10, 0, -1)
    ```python
    for num in range(1, 10, 2):
        print(num)
    ```

- while - expressão booleana
    - sendo o loop repetido ate a expressão for verdadeira
    - expressão booleana é toda expressão que o resultado é verdadeiro ou falso
    - em um loop while é importante que o criterio se torne falso em algum momento 
        - esse criterio que sera de incrementação vai ao final 
    - no python não tem a expressão do while

```python
numero = 1

while numero < 10:
    print(numero)
    numero = numero +1
```
```python
resposta= ''

while resposta != 'sim':
    resposta = input('ja acabou jessia? ')
```


- sair do loop com o break, é sair de maneira projetada
```python
for numero in range(1, 11):
    if numero == 6:
        break
    else:
        print(numero)
print('sai do loop')
```

```python
while True:
    comando = input('digite sair pra sair: ')
    if comando == 'sair':
        break    
```

# SEÇÃO 7: COLEÇÕES PYTHON

## listas
- funciona como arrays em outras linguagens, com a diferença de ser dinamica e poder colocar qualque rtipo de dado 
- dinamico pq não possui tamanho fisico
- as listas não possuem tipo de dado fixo
- representadas por []

```python
lista = list(range(11))
```


```python
if 8 in lista:
    print('encontrei o numero')
else:
    print('não encontrei o numero')
```

- lista.sort() - irá ordenar a lista

- contar quantas vezes um elemento aparece >> lista.count(elemento)

- incluir novos elementos >> lusta.append(novo_elemento)
    - é possivel colocar uma lista dentro de outra lista

- pode se determinar a posição do novo elemento >> lista.insert(posição, novo_elemento)
    - deslocando os demais elementos para a direita da lista

- pode somar as listas >> lista1= lista1 + lista2

- pode reverter uma lista >> lista.reverse() -- com () vazios ou [::-1]

- para copiar uma lista >> lista6 = lista2.copy()

- len(lista) - para saber o numero de elementos de dentor da lista

- lista.pop() >> remove o ultimo elemento e  retorna 
    - se pode remover pelo inidice >> lista.pop(2)

- para remover todos os elementos >> lista.clear()

- para repetir os elementos da listas é só multiplicar a lista >>> lista = lista *3

- converter uma string para uma lista, separando os elementos da lista pelo o espalo entre elas
    - entre os () se pode especificar outro tip de separador exemplo (,)
   ```python
   curso = 'programação python'
   curso2 = curso.split()
    ```    

- para faezr ao contrario, converter uma lsita em uma string se utiliza o join  
    ```python
    lista = ['programação', 'python']
    curso = ' '.join(lista)
    # estamos falando pega a lista pega espaço em cada elemento e transforma em uma string
    ```

- ha a possibilidade de criar listas om variaveis
   ```python
    cores = ['verde', 'amarelo', 'azul']
    print(cores[0])
    print(cores[1])
    ```

- para somar string em uma lista
```python
lista = ['i', 'l', 'o', 'v', 'e', 'y', 'o', 'u']
soma = ' '
for elemento in lista:
    print(elemento)
    soma = soma + elemento
print (soma)
```

- para imprimir com o indice
```python
cores = ['verde', 'amarelo', 'azul']
for indice, cor in enumerate(cores):
    print(indice, cor)
```

- encontrar o indice de um elemento na lista >> index
    - print(lista.index(indice_desejado))
    - pode pedir pra buscar a aprtir de um indice em especifico com range
        - print(numeor.index(5, 1)) #busca apartir do indice 1
        - print(numeor.index(5, 6, 8)) #busca entr o indice  6 e 8 


- procurar valor max, min, e tamanho da lista
    - print(sum(lista)) - soma
    - print(max(lista)) - valor maximo
    - print(min(lista)) - valor minimo
    - print(len(lista)) - tamanho da lista

## tuplas
- parecidas com listas, mas representadas por parentenses (); são imutaveis; python não reconhece como tupla se não tiver virgula, esta é a sua definiçãop não os ()
    - utilizar sempre que não precisamos ou devemos modificar os dados de uma coleção, por exemplo, meses do ano
    - tuplas são mais rapidas do que listas
    - mais segurança por que são imutaveis
    - (4) - não é tupla; (4, ) é uma tupla

- a concatenação de tuplas é pssovel na criação de uma nova tupla ou na sua sobre escrita; tupla1 = tupla1 + tupla2

```python
# para contar elementos em uma tupla

tupla = ('a', 'b', 'c', 'd', 'e', 'a', 'b')

print(tupla.count('c'))
```

```python
#imprimir indice e valor

tupla = (1, 2, 3)

for indice, valor in enumerate(tupla):
    print(indice, valor)
```

```python
meses=('janeiro', 'fevereiro', 'março', 'abril', 'maio', 'junho', 'julho', 'agosto', 'setembro', 'outubro', 'novembro', 'dezembro')

# imprimir em cada linha
i=0

while 1<len(meses):
    print(meses[i])
    i=i+1

# saber o indice de algum elemento
print (mese.index('junho')) #se não existir o elemento o resultado é erro
```

- é possivel o slicing, o pulo
    - tupla(inicio: fim: passo)

```python


```




```python
```
# SEÇÃO 8: FUNÇÕES EM PYTHON
- definindo funções
    -   pequenas partes que executando uma tarefa específica
    - pode ou não receber entrada de dados e retornar uma saida de dados
    - muitos uteis para executar procdimentos similares por repetidas vezes
    - a função da função é dry - não repetir o seu codigo
- função integrada é uma built-in
- nome da função sempre com letra minusculo e separa por underline
    - parametros de entrada são opcionais e se tiver mais de um será separada por virgula
    - o parametro pode não ter retorno 
- para executar uma função se faz necessário chmar pelo nome e utilizar () colado no nome, sem espaço

-podemos criar variaveis do tipo de uma função e executar esta função atraves da variavel

```python
# forma geral de defnição

def mome_funcao(parametros_entrada):
    bloco_funcao
```

```python
#exemplo

def diz_oi():
    print('oi')

# há a possibilidade de ter uma função dentor de outra
# esta função executa uma tarefa
#esta função nao recbe parametro de entrada
# esta função não retorna nada

## para utilizar se faz necessário a sua chamada- nome +()

diz_oi()
```

```python
#exemplo 2
def cantar_parabens():
    print('parabens pra vc')
    print('nesta data querida')
    print('muitas felicidades')
    print('muitos anos de vida')
    
for n in range(5):
    cantar_parabens()
```

```python
#-podemos criar variaveis do tipo de uma função e executar esta função atraves da variavel
canta= cantar_parabens

canta()
```

-- funções com retorno
    - quando uma função não retorna nenhum valor o retorno é none
    - funções que retornam valores, devem retornar estes valores com a palavra reservada return
    - não necessariamente precisamos criar uma variavel para receber o retorno de uma função. Podemos passar a execução da função para outras funções 
    - o return finaliza a função, ou seja, sai da execução da função
    - podemos ter mais de um return na função
    - podemos em uma função retornar qualquer tipo de dados, ate multiplos valores

```python
def quadrado_7():
    return 7*7

ret=quadrado_7()

print(f'retorno {ret}')

#ou
print(f'Retorno {quadrado_7}')
```

```python
def diz_oi():
    return 'oi'

alguem = 'pedro'

print(diz_oi() + alguem)

# se estive print ao inves de return daria erro, pq o retorno do print na função seria none e não se pode somar nada com a string da variavel
```


```python
def diz_oi():
    return 'oi'
    print('sendo execuado depois do retorno')

# esse print não será executado pq o retorno finaliza a função
```


```python
# para testar onde a função é encerrada

def nova_função():
    variavel = True #ou None 
    if variavel: # xecutada se a variavel for =True
        return 4
    elif variavel is None:
        return 3.2
    return 'b'
```


```python
#função para jogar a moeda

from random import random

def joga_moeda():
    valor=random()
    if valor > 0.5:
        return 'cara'
    return 'coroa'

print(joga_moeda())

# se observa que não há necessidade de colocar o else
```

-- funções com parametros
    - fuções que recebem dados para serem processados dentro da mesma

```python
def quadrado(numero):
    return numero * numero

print(quadrado(7))
print(quadrado(5))
```


```python
def cantar_parabens(anivesariante):
    print('parabens pra vc')
    print('nesta data querida')
    print('muitas felicidades')
    print('muitos anos de vida, {aniversariante}')
    
cantar_parabens('Marcos')

#se estiver em branco, (), não irá executar pq o parametro é obrigatório
```


```python
def soma(a, b):
    return a+b

def multiplica(num1, num2):
    return num1*num2

def outra(num1, b, msg):
    return (num1 +b)*msg


print(soma(2, 5))

print(multiplica(2, 8))

print(outra(3, 2, 'geek'))

#se for informado um numero errado de parametro ou argumento teremos typeerror
```


-- nomeando parametros
    - o nome deve corresponder a utilização do item

- parametros são variaveis declradas na definição de uma função
- argumentos são dados passados durante a execução deuma função

- argumento nomeados
    - caso utilizemos nomes dos parametros nos argumentos para informa-los podemos utilizar em qualquer ordem, pq vc estará especificando o valor do parametro e não a ordem dele 

```python
def nome_completo(nome, sobrenome): #parametros
    return f'{nome} {sobrenome}' 

print(nome_completo('jessica', 'fernandes')) # argumentos

# exemplo de argumento nomeado
print(nome_completo(nome='maria', sobrenome='lima'))
```


-- função com parametro padrão
    - função onde a passagem de parametro seja opcional
    - exemplo o print com () vazio é ignorado
    - parametro definidos na função são obrigatorios para funcionar

- os parametros informados como padrão são definidos ao final

- se tiver um variavel local (dentro da função) com o mesmo nome de uma variavel global, a local terá preferencia com a global sendo ignorada
    - com funções é importante evitar a variavel global
    - para utilizar necessário declarar ela como global >> global nome_variavel
    - se for uma função dentro de outra função, e nesta segunda função for utilizado variavel da primeira função a forma de declaração é nonlocal >> nonlocal nome_variavel

```python
def exponencial(numero, potencial): # parametros obrigatorio
    return nuemro **potencia
print(exponencial(2,3))


# nesse segundo exemplo o parametro numero é obrigatorio informar e o potencial se não for informado será utilizado o 2 como padrão
def exponencial(numero, potencial=2): #parametro padrão informado no final
    return nuemro **potencia

print(exponencial(2))
```

```python
def soma(num1, num2):
    return num1+num2

def mat(num1, num2, fun=soma): #um dos parametros é a função desejada que s enão especificada será utilizada a soma
    return fun(num1, num2)

def subtracao(num1, num2):
    return num1-num2

print(mat(2,3))
print(mat(2, 2, subtracao))
```

```python
# exemplo de erro pela variavel ter sido iniciada fora da função

total =0

def incrementa():
    total = total +1
    return total

print(incrementa)

# forma de arrumar é declarar que a variavel é global
total =0

def incrementa():
    global total # aviso da variavel global
    total = total +1
    return total

print(incrementa)
```

- documentando funções om docstrings
    - se colocar um comentário com """ dentro da função, vc está documentando aquela função, assim se no terminal for utilizado o help(nome_função) irá aparecer o comentário inserido
    - ou tbm com o comando >> print(nome_função.__doc__)


- *args
    - é um parametro como outro qualquer, pode chamar de qualquer coisa desde que começa com *
    - utilizado em um função, coloca os valores extras informados como entrada em uma tupla
    - tupla são imutaveis
    - pode ser utilizado para não limitação de parametros ou como verificor de informação

```python
def soma_numeros(num1, num2, num3):
    return num1+num2+num3

print(soma_numeros(4, 6, 9))


# com *args
def soma_numeros(*args):
    total=0
    for numero in args:
        total=total+numero
    return

print(soma_numeros())
print(soma_numeros(1))
print(soma_numeros(2,3,6,8,9))

# ou ainda
def soma_numeros(*args):
    return sum(arg)

print(soma_numeros())
print(soma_numeros(1))
print(soma_numeros(2,3,6,8,9))
```

```python
def verifica_info(*args):
    if 'geek' in arg and 'university' in args:
        return 'bem vindo nerd'
    return 'eu não sei quem vc é...'

print(verifica_info())
print(verifica_info(1,  True, 'university', 'geek'))
print(verifica_info(1, 'university', 3.145)
```

- **kwargs
    - o nome poderia ser qualquer um desde que iniciado com **, utiliza kwargs por confensão
    - como o args é mais parametro, mas ao inves de se tornar uma tupla, transforma em um dicionario
    - transforma em um dicionario pq utiliza parametros nomeados, pegando chave e valor por tanto

```python
def cores_favoritas(**kwargs):
    for pessoa, cor in kwargs.items():
        print('a cor favorita de {pessoa} é {cor}')

cor_favorita(marcos='verde', julia='amarelo', fernanda='azul', vanessa='branco')
```


- nas funções podemos ter e precisam ser escritos nessa ordem
    - parametros obrigatórios
    - *args
    - parametros default (não obrigatórios)
    - **kwargs

- 


- desempacotar com **kwargs

```python
def mostra_nomes(**kwargs):
    return f"{kwargs['nome']} {kwargs['sobrenome']}"

nomes = {'nome':'felicity', 'sobrenome':'jones'}

print(mostra_nomes(**nomes))
```






```python
```

# SEÇÃO 9: COMPREHENSIONS EM PYTHON
- dimunir as linhas de codigo


# SEÇÃO 10: EXPRESSÕES LAMBDAS E FUNÇÕES INTEGRADAS

# SEÇÃO 11: DEBUGANDO E TRATANDO ERROS

# SEÇÃO 12: TRABALHANDO COM MÓDULOS PYTHON

# SEÇÃO 13: LEITURA E ESCRITA EM ARQUIVOS

# SEÇÃO 14: ITERADORES E GERADORES PYTHON

# SEÇÃO 15: DECORADORES EM PYTHON

# SEÇÃO 16: ORIENTAÇÃO A OBJETOS COM PYTHON

# SEÇÃO 17: HERANÇA E POLIMORFISMO

# SEÇÃO 18: MANIPULANDO ARQUIVOS CSV E JSON

# SEÇÃO 19: TRABALHANDO COM DATA E HORA EM PYTHON

# SEÇÃO 20: TESTES COM PYTHON

# SEÇÃO 21: GERENCIAMENTO DE MEMÓRIA EM PYTHON

# SEÇÃO 22: CHEGAGEM DE TIPOS EM PYTHON



# SEÇÃO 23: NOVIDADES DO PYTHON 3.8

## operador walrus :=
- permite realizar atribuição e retorno de valor em uma mesma expressão
    - variavel:= expressão

```python
nome = 'roberto'
print(nome)

# com o novo operador fica
print(nome := 'roberto')
```

```python
cesta = [] #lista vazia
fruta = input('informe a fruta: ')

while fruta != 'jaca': #enquanto fruta for diferente de jaca
    cesta.append(fruta) #incluir fruta na lista cesta
    fruta = input('informe a fruta: ')

# nova forma de realizar o codigo
cesta = []
while (fruta := input('informe a fruta: ')) != 'jaca':
    cesta.append(fruta)
```

## argumentos somente posicionais
- é utilizado a / para dizer que o que esta antes é apenas posicional
- havendo mais um ponto a ser declarado posicional só colocar uma / ao final de tudo e não de cada

```python
def cumprimenta(nome, /):
    return f'ola {nome}'

print(cumprimenta('jessi')) #ira se rexecutado
print(cumprimenta(nome='jessi')) #não será pq na definição da função foi colocado que nome é apenas posição
```


# SEÇÃO 24: PROJETO PYTHON 1 - GAME
# SEÇÃO 25: PROJETO PYTHON 2 - MERCADO
# SEÇÃO 26: PROJETO PYTHON 3 - BANCO


# SEÇÃO 27: ENCERRAMENTO
- realizado
