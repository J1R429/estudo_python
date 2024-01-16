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



12+127+101+95
# SEÇÃO 6: ESTRUTURAS DE REPETIÇÃO EM PYTHON
# SEÇÃO 7: COLEÇÕES PYTHON
# SEÇÃO 8: FUNÇÕES EM PYTHON
# SEÇÃO 9: COMPREHENSIONS EM PYTHON
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
# SEÇÃO 24: PROJETO PYTHON 1 - GAME
# SEÇÃO 25: PROJETO PYTHON 2 - MERCADO
# SEÇÃO 26: PROJETO PYTHON 3 - BANCO
# SEÇÃO 27: ENCERRAMENTO











