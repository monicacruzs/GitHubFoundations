# 2. Comandos Essenciais do Git

Nesta seção, você aprenderá os comandos essenciais do Git que são fundamentais para trabalhar com repositórios e gerenciar seu código de forma eficiente.

# 2.1. Inicializando um Repositório
Para começar a trabalhar com o Git em um novo projeto, é necessário inicializar um repositório. Isso cria a estrutura básica que o Git usa para rastrear as mudanças no seu projeto.

```bash
git init
```

Este comando inicializa um repositório Git na pasta atual. A partir desse momento, o Git começará a rastrear todas as alterações feitas nos arquivos dessa pasta.

# 2.2. Clonando um Repositório
Para trabalhar em um projeto existente, você precisa criar uma cópia local do repositório do GitHub. Para isso, use o comando:

```bash
git clone <url-do-repositorio>
```
Este comando cria uma cópia do repositório remoto em sua máquina. A <url-do-repositorio> deve ser substituída pela URL do repositório que você deseja clonar.

# 2.3. Adicionando Mudanças ao Stage
Antes de fazer um commit, é necessário adicionar as mudanças ao stage. Isso permite que você selecione quais mudanças serão incluídas no próximo commit.

```bash
git add <arquivo-ou-diretorio>
```
Este comando adiciona um arquivo ou diretório específico ao stage. Para adicionar todas as mudanças:

```bash
git add .
```

# 2.4. Fazendo um Commit
Depois de adicionar as mudanças ao stage, você pode criar um commit, que é uma "foto" do seu código em um momento específico.

```bash
git commit -m "Mensagem descrevendo as mudanças"
```

A mensagem deve ser clara e descrever o que foi alterado nesse commit.

# 2.5. Enviando Mudanças para o GitHub
Após fazer o commit, você precisa enviar as mudanças para o repositório remoto no GitHub:

```bash
git push origin main
```

Aqui, origin é o nome padrão para o repositório remoto, e main é a branch principal.

# 2.6. Atualizando Seu Repositório Local
Para garantir que você está trabalhando com a versão mais recente do código, é importante atualizar seu repositório local:

```bash
git pull origin main
```

Este comando baixa e aplica as mudanças do repositório remoto à sua cópia local.

# 2.7. Verificando o Status do Repositório
Para verificar o status do seu repositório, use:

```bash
git status
```

Este comando mostra quais arquivos foram modificados, quais estão no stage e quais não foram rastreados pelo Git.

# 2.8. Visualizando o Histórico de Commits
Para visualizar o histórico de commits e as mudanças feitas ao longo do tempo:

```bash
git log
```

Este comando exibe uma lista de commits com suas respectivas mensagens, autor e data.

# 2.9. Trabalhando com Branches
Branches permitem que você trabalhe em diferentes partes do seu projeto de forma isolada.

Criar uma nova branch:

```bash
git branch <nome-da-branch>
```

Mudar para uma branch existente:

```bash
git checkout <nome-da-branch>
```

Fundir uma branch à branch principal:

```bash
git merge <nome-da-branch>
```

