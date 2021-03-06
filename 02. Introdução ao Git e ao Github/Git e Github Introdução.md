# Introdução ao Git e Github
## Professor Otávio Reis

### Definição:

É um Sistema de Controle de Versões distribuídos.

### Características:

1. Controle de Versão
2. Armazenamento em Nuvem
3. Trabalho em Equipe
4. Melhorar seu Código
5. Reconhecimento

### Instalações Necessárias:

Baixar de acordo com o Sistema Operacional.

- [Git](https://git-scm.com/)

### Dicas de uso de Terminal:

##### Windows

- cd
- dir
- mkdir
- del/ rmdir

##### Unix

- cd
- ls
- mkdir
- rm -rf

##### Criar arquivo: echo nome_do_arquivo > nome_do_arquivo.extensão

##### Delete Arquivo: del nome_do_arquivo.extencao

##### Delete pasta: rmdir nome_da_pasta /S /Q

### Importante Conhecer:

- SHA1:
  * possui hash seguro
  * funções da NSA (Agência de Segurança Nacional dos EUA)
  * gera caracteres de 40 dígitos
- Objetos Fundamentais:
  * BLOBS (Arquivos) = conteúdo
  * TREES (Árvores) = armazenam BLOBS
  * COMMITS = único para cada autor
    * TREE
    * PARENTE
    * Autor
    * Mensagem
    * Timestamp (data/hora)

### GIT (Distribuído e Seguro)

- contém todas as característica citadas acima.

### Criando uma chave SSH:

- Entre no seu Github
  * Entre no Perfil
  * Vá até Settings
  * Procure por SSH and GPS
  * Clique para criar uma Nova Chave

- No GitBash:
  * Digite: ssh-keygen -t ed25519 -C seuemail@email.com
  * ENTER
  * Navegue até a pasta onde foi criado o arquivo.
  * Digite: cat id_ed25519.pub
  * ENTER
  * copie a chave que aparecer na tela.

- No Github:
  * Digite um título
  * colar chave criada lá no GitBash

- Volte ao GitBash:
  * Digite: eval $(ssh-agent -s)
  * ENTER
  * Digite: ssh-add id_ed25519
  * ENTER

Fim, sua chave já está ativa!

### Documentação:

- [Gerar uma nova chave SSH] (https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
- [Outros assuntos] (https://docs.github.com)

### Token de Acesso Pessoal

- No Github
  * Vá em Perfil
  * Settings
  * Procure por Personal Acess Tokens
  * Clique em Gerar Token
  * De um Nome
  * Em Expirações: Escolha um tempo
  * Em Select Scopes - selecione (marque) repo
  * Clique em gerar token
  * Copie o token para que não ocorra esquecimento.
  * Após isso não será mais exibido o token.

Use o token no lugar da senha.
Automaticamente o Git saberá se você possui um token.


### Comandos do Git

- Comandos básicos:
  * ls (lista)
    * ls -a (lista arquivos ocultos)
  * ctrl+l (limpa)

- Comando da máquina local:
  * git init
  * git add . ou git add *
  * git commit -m "mensagem"

- Comandos acesso usuário:
  * git config --global user.nome "NOME IGUAL AO QUE ESTÁ NO GITHUB"
  * git config --global user.email "EMAIL IGUAL AO QUE ESTÁ NO GITHUB" 

- Comandos listar configurações:
  * git config --list
  * q para sair

- Desloga usuário:
  * git config --global -unset user.nome "NOME IGUAL AO QUE ESTÁ NO GITHUB"
  * git config --global -unset user.email "EMAIL IGUAL AO QUE ESTÁ NO GITHUB" 

- Comando caso haja conflitos:
  * git pull
  * altere o arquivo e dê um git add . e um commit

- Verificar Status:
  * git status

- Comando para clonar arquivo remoto para máquina local:
  * git clone https://github.com/owner/seu_repositorio.git

- Comando para colocar o dados no Servidor do Github:
  * git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME.git

### Ciclo que ocorre na máquina local

1. Unmodified (Sem alteração)
2. Modified (Modificado)
3. Staged (Recebe os dados)