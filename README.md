Atividade de Gerência e configuração de serviços de Internet, lecionada pelo professor Rhavy Maia, na graduação do curso de Tecnologia em Sistemas de Internet. A seguir vamos ao um tutorial para a criação de uma pipeline de integração e entrega contínua no Jenkins para uma aplicação de serviço restful que utiliza o framework Flask-restful. Essa pipeline deve ter duas etapas: construção (build) e teste. A pipeline deve ser definida no arquivo Jenkinsfile que estará dentro do projeto.

# Criação de uma pipeline de Jenkins

A seguir um guia para execução da pipeline

1.Navegue até o diretório  usando o comando:

`cd /var/run/`

2.Garanta permissões no seguinte arquivo:

`sudo chmod 777 docker.sock`

# Criando uma pipeline

1.Faça login no jenkins e clique em `+Novo Item`;

2.Crie um nome para sua pipeline, e selecione `pipeline` e clique em `OK`;

3.Adicione uma descrição;

4.Na seção Pipeline, em `definição` selecione `Pipeline script from SCM`;

5.Na mesma seção, SCM selecione `Git` e em Repository URL adicione a seguinte URL `https://github.com/liliamariamelo/pipeline-jenkins.git` ;

6.Na Branch Specifier defina `*/main` e no final da página clique em `Salvar` .

# Implementação da pipeline

1.No lado esquerdo clique em `Build Now` e em seguida, clique em `Open Blue Ocean`;

2.Clique na pipeline criada e verifique o build e test, e pronto pipeline criada com sucesso!