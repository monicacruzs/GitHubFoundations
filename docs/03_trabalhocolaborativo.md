# 3. Trabalho Colaborativo no GitHub

## 3.1. Pull Requests
Um Pull Request (PR) é uma forma de propor mudanças em um repositório. Ele permite que outras pessoas revisem e discutam as alterações antes de incorporá-las ao código principal. Para criar um Pull Request:

### Primeiro, faça suas mudanças em uma branch separada.
```bash
git checkout -b minha-branch 
```

### Depois de fazer as alterações, adicione e comite as mudanças.
```bash
git add .
git commit -m "Descreva as mudanças feitas"
```

### Envie a branch para o GitHub.
```bash
git push origin minha-branch
```

### No GitHub, vá até o repositório e clique em "New Pull Request".

## 3.2. Forks e Clones
Um Fork é uma cópia de um repositório que permite a você experimentar mudanças sem afetar o original. Use um Fork quando quiser contribuir para um projeto que não seja seu. Já o Clone é uma cópia local de um repositório. Para criar um Fork e clonar o repositório:


### No GitHub, clique em "Fork" no repositório desejado.

### Para clonar o repositório Forkado localmente:

```bash
git clone <url-do-repositorio-forkado>
```

## 3.3. Issues e Projects
Issues são uma forma de rastrear tarefas, melhorias ou bugs. Elas permitem discussões sobre o que precisa ser feito. Já os Projects no GitHub ajudam a organizar e priorizar essas tarefas em um formato visual, como um Kanban.

Para criar uma Issue:

# No GitHub, vá até a aba "Issues" e clique em "New Issue".
Para organizar tarefas em um Project:


# No GitHub, vá até a aba "Projects" e crie um novo projeto.
# Adicione as issues ou tarefas necessárias no quadro do projeto.

## 3.4. GitHub Actions
GitHub Actions permite a automação de fluxos de trabalho, como testes e deploys automáticos, diretamente no repositório. Para configurar uma ação simples:

```yaml
### No repositório, crie uma pasta .github/workflows e dentro dela um arquivo .yml com o seguinte conteúdo:

name: CI

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - name: Run a one-line script
      run: echo Hello, world!
````

Esse exemplo básico executa um script simples sempre que há um push ou pull request.
