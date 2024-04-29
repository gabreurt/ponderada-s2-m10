# Relatório: Compilação e Execução do Backstage

## Introdução
Este relatório descreve o processo de compilação e execução da ferramenta Backstage, seguindo as instruções fornecidas no tutorial "Installing a standalone server" & "Building a Docker image" disponibilizado no site do Backstage.

## Passo 1: Preparação do Ambiente
Antes de iniciar o processo de compilação e execução, verifiquei se meu sistema atende aos pré-requisitos listados no tutorial, incluindo acesso a um sistema operacional baseado em Unix, instalação do Node.js, Yarn, Docker, Git, entre outros.

## Passo 2: Criação do Aplicativo Backstage
Utilizei o comando `npx @backstage/create-app@latest` para criar um novo aplicativo Backstage.

## Passo 3: Execução do Aplicativo Backstage
Naveguei até o diretório do aplicativo Backstage criado.
Executei o comando `yarn dev` para iniciar o aplicativo Backstage.
Aguardei até ver a mensagem `[0] webpack compiled successfully`.

## Passo 4: Construção da Imagem Docker
No diretório raiz do repositório, executei os comandos `yarn install --frozen-lockfile`, `yarn tsc` e `yarn build:backend --config ../../app-config.yaml` para instalar as dependências e construir o backend.
Construí a imagem Docker usando o Dockerfile fornecido no guia.
Executei a imagem Docker localmente usando o comando `docker run -it -p 7007:7007 backstage.` e acessei a aplicação no endereço URL `http://localhost:7007/`

## Prints

### Arquivo dockerfile e estrutura de arquivos
![Arquivo dockerfile](assets/Captura%20de%20tela%202024-04-29%20000858.png)

<br>

### Aplicação rodando no docker
![Aplicação rodando no docker](assets/Captura%20de%20tela%202024-04-29%20001039.png)

<br>


### Aba de componentes
![Aba de componentes](assets/Captura%20de%20tela%202024-04-29%20000356.png)


<br>

### Página inicial da aplicação no docker
![Página inicial da aplicação no docker](assets/Captura%20de%20tela%202024-04-29%20000327.png)