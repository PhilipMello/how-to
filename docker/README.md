# Como Utilizar o Docker

## Referência de Documentação do Docker

[Documentação de Referência do Docker](https://docs.docker.com/reference/ "Documentação de Referência")

## Imagens Docker

### Login no CLI do Docker

```bash
docker login

Baixar Imagens do Docker

docker pull "nome-da-imagem"

Exemplo: docker pull ubuntu

Exibir Imagens do Docker

docker image ls
ou
docker images

Remover uma ou Mais Imagens

docker image rm "nome-da-imagem"

Exemplo: docker image rm ubuntu

ou

docker rmi "nome-da-imagem"

Exemplo: docker rmi ubuntu

docker image rm "nome-da-imagem"

Exemplo: docker image rm ubuntu

ou

docker rmi "nome-da-imagem"

Exemplo: docker rmi ubuntu

Remover Imagens Não Utilizadas (CUIDADO, ESSE COMANDO IRÁ REMOVER TODAS AS IMAGENS DO DOCKER NO COMPUTADOR)

docker image prune

Enviar Imagem Docker para o DockerHub

docker push "nome-da-imagem"

Exemplo: docker push ubuntu

Inspecionar Imagem Docker

docker image inspect "nome-da-imagem"

Exemplo: docker image inspect ubuntu

Construir Imagem Docker

docker image build "nome-da-imagem"

Exemplo: docker image build ubuntu

docker image build "nome-da-imagem"

Exemplo: docker image build ubuntu

Contêiner Docker
Listar Todos os Contêineres em Execução

docker container ps
ou
docker ps

Listar Todos os Contêineres

docker container ps -a
ou
docker ps -a
ou
docker ps --all

Parar um Contêiner Docker

docker container stop "id-do-contêiner"
ou
docker container stop "nome-do-contêiner"
ou

docker stop "id-do-contêiner"
ou
docker stop "nome-do-contêiner"

Copiar Arquivos para o Contêiner Docker

docker container cp

Exemplo: docker container cp arquivo.txt abcdocker889938:/usr/share

docker container cp

Exemplo: docker container cp arquivo.txt abcdocker889938:/usr/share


Com essa formatação, o GitHub destacará corretamente a sintaxe de cada bloco de código, tornando-o mais fácil de ler e entender.



