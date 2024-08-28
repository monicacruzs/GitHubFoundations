# 2. Comandos Essenciais do Git

Nesta seção, você aprenderá os comandos essenciais do Git que são fundamentais para trabalhar com repositórios e gerenciar seu código de forma eficiente.

## 2.1. Inicializando um Repositório

Para começar a trabalhar com o Git em um novo projeto, é necessário inicializar um repositório. Isso cria a estrutura básica que o Git usa para rastrear as mudanças no seu projeto.

```bash
git init
```

Este comando inicializa um repositório Git na pasta atual. A partir desse momento, o Git começará a rastrear todas as alterações feitas nos arquivos dessa pasta.

### Exibindo a Versão do Git

Para verificar a versão do Git instalada na sua máquina:

```bash
git version
```

Este comando é útil para garantir que você está utilizando a versão correta do Git.

## 2.2. Configurando o Git

Antes de começar a usar o Git, é importante configurar seu nome de usuário e e-mail:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

Para visualizar as configurações ativas do Git:

```bash
git config --list
```

Essas configurações garantem que seus commits sejam atribuídos corretamente a você.

## 2.3. Clonando um Repositório

Para trabalhar em um projeto existente, você precisa criar uma cópia local do repositório do GitHub. Para isso, use o comando:

```bash
git clone <url-do-repositorio>
```

Este comando cria uma cópia do repositório remoto em sua máquina. A \`<url-do-repositorio>\` deve ser substituída pela URL do repositório que você deseja clonar.

## 2.4. Adicionando Mudanças ao Stage

Antes de fazer um commit, é necessário adicionar as mudanças ao stage. Isso permite que você selecione quais mudanças serão incluídas no próximo commit.

```bash
git add <arquivo-ou-diretorio>
```

Este comando adiciona um arquivo ou diretório específico ao stage. Para adicionar todas as mudanças:

```bash
git add .
```

## 2.5. Fazendo um Commit

Depois de adicionar as mudanças ao stage, você pode criar um commit, que é uma "foto" do seu código em um momento específico.

```bash
git commit -m "Mensagem descrevendo as mudanças"
```

A mensagem deve ser clara e descrever o que foi alterado nesse commit.

## 2.6. Enviando Mudanças para o GitHub

Após fazer o commit, você precisa enviar as mudanças para o repositório remoto no GitHub:

```bash
git push origin main
```

Aqui, \`origin\` é o nome padrão para o repositório remoto, e \`main\` é a branch principal.

## 2.7. Atualizando Seu Repositório Local

Para garantir que você está trabalhando com a versão mais recente do código, é importante atualizar seu repositório local:

```bash
git pull origin main
```

Este comando baixa e aplica as mudanças do repositório remoto à sua cópia local.

## 2.8. Verificando o Status do Repositório

Para verificar o status do seu repositório, use:

```bash
git status
```

Este comando mostra quais arquivos foram modificados, quais estão no stage e quais não foram rastreados pelo Git.

## 2.9. Visualizando o Histórico de Commits

Para visualizar o histórico de commits e as mudanças feitas ao longo do tempo:

```bash
git log
```

Este comando exibe uma lista de commits com suas respectivas mensagens, autor e data.

## 2.10. Visualizando Diferenças

Para comparar as mudanças feitas nos arquivos:

```bash
git diff
```

Este comando mostra as diferenças entre o estado atual dos arquivos e o último commit.

## 2.11. Trabalhando com Branches

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

## 2.12. Revertendo Mudanças

Se precisar desfazer um commit ou voltar a um estado anterior, você pode usar:

```bash
git revert <hash-do-commit>
```

Para resetar o estado do repositório a um ponto anterior, use:

```bash
git reset <hash-do-commit>
```

## 2.13. Trabalhando com Tags

Tags são usadas para marcar pontos específicos na história do repositório, como versões:

```bash
git tag <nome-da-tag>
```

Tags ajudam a identificar versões específicas do seu projeto.

# 2.12. Gerenciando Repositórios Remotos

Para colaborar com repositórios remotos, como os hospedados no GitHub, é importante saber gerenciar essas conexões:

```bash
git remote -v
```
Este comando lista os repositórios remotos associados ao seu repositório local, mostrando suas URLs para push e pull.

Para adicionar um novo repositório remoto:

```bash
git remote add origin <url-do-repositorio>

Substitua <url-do-repositorio> pela URL do repositório remoto. O nome origin é um alias comum para o repositório remoto principal.

```
Para remover um repositório remoto:

```bash
git remote remove <nome-do-remoto>
```
Este comando remove a conexão com o repositório remoto especificado.



