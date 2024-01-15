[SEÇÃO 1: APRESENTAÇÃO](#seção-1:-apresentação)
[SEÇÃO 2: PREPARANDO O AMBIENTE](#seção-2:-preparando-o-ambiente)
[SEÇÃO 3: INTRODUÇÃO Á LINGUAGEM PYTHON](#seção-3:-introdução-á-linguagem-python)
[SEÇÃO 4: VARIÁVEIS E TIPOS DE DADOS EM PYTHON]
[SEÇÃO 5: ESTRUTURAS LÓGICAS E CONDICIONAIS EM PYTHON]
[SEÇÃO 6: ESTRUTURAS DE REPETIÇÃ EM PYTHON]
[SEÇÃO 7: COLEÇÕES PYTHON]
[SEÇÃO 8: FUNÇÕES EM PYTHON]
[SEÇÃO 9: COMPREHENSIONS EM PYTHON]
[SEÇÃO 10: EXPRESSÕES LAMBDAS E FUNÇÕES INTEGRADAS]
[SEÇÃO 11: DEBUGANDO E TRATANDO ERROS]
[SEÇÃO 12: TRABALHANDO COM MÓDULOS PYTHON]
[SEÇÃO 13:]
[SEÇÃO 14:]
[SEÇÃO 15:]
[SEÇÃO 16:]
[SEÇÃO 17:]
[SEÇÃO 18:]
[SEÇÃO 19:]
[SEÇÃO 20:]
[SEÇÃO 21:]
[SEÇÃO 22:]
[SEÇÃO 23:]
[SEÇÃO 24:]
[SEÇÃO 25:]
[SEÇÃO 26:]
[SEÇÃO 27:]


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

# SEÇÃO 3: INTRODUÇÃO Á LINGUAGEM PYTHON
