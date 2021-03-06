# Docker
Step by step
________________________
Neste passo-a-passo, será visto como instalar o Docker no Ubuntu 64 bits. Todos os comandos listados devem ser executados no seu terminal.

Antes de mais nada, remova possíveis versões antigas do Docker:

```
sudo apt-get remove docker docker-engine docker.io
```
Depois, atualize o banco de dados de pacotes:
```
sudo apt-get update
```
Agora, adicione ao sistema a chave GPG oficial do repositório do Docker:
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add 
```
Adicione o repositório do Docker às fontes do APT:
```
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
   ```
Atualize o banco de dados de pacotes, pare ter acesso aos pacotes do Docker a partir do novo repositório adicionado:
```
sudo apt-get update
```
Por fim, instale o pacote docker-ce:
```
sudo apt-get install docker-ce
```
Caso você queira, você pode verificar se o Docker foi instalado corretamente verificando a sua versão:
```
sudo docker version
```
E para executar o Docker sem precisar de sudo, adicione o seu usuário ao grupo docker:
```
sudo usermod -aG docker $(whoami)
```

Fonte: [Alura.com.br](https://cursos.alura.com.br/course/docker-e-docker-compose/task/28593)
