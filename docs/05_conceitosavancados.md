# 5. Conceitos Avançados

## 5.1. Git Tag
O *tag* no Git é usado para marcar pontos específicos na história do repositório, como versões lançadas. É uma maneira de identificar facilmente estados importantes do projeto. Para criar e usar tags:

1. **Criar uma tag anotada**:
```bash
git tag -a v1.0 -m "Versão 1.0"
```
   Aqui, v1.0 é o nome da tag e "Versão 1.0" é uma mensagem descritiva.

2. Criar uma tag leve (sem mensagens adicionais):

```bash
git tag v1.0
```

3. Listar todas as tags:

```bash
git tag
```

4. Enviar tags para o repositório remoto:

```bash
git push origin v1.0
```

Para enviar todas as tags:

```bash
git push --tags
```

5. Mostrar informações sobre uma tag:

```bash
git show v1.0
```

## 5.2. Submodules
Submodules permitem que você mantenha um repositório Git dentro de outro repositório Git. Eles são úteis para projetos que dependem de outros projetos.

1. Adicionar um submódulo:

```bash
git submodule add <url-do-repositorio>
```

2. Inicializar submódulos existentes (quando você clona um repositório que já contém submódulos):

```bash
git submodule init
git submodule update
```

3. Atualizar submódulos:

```bash
git submodule update --remote
```

4. Remover um submódulo:

Remova a entrada do submódulo no arquivo ```.gitmodules```.
Remova a entrada do submódulo no arquivo ```.git/config```.

Execute:

```bash
git rm --cached <caminho-do-submodulo>
rm -rf <caminho-do-submodulo>
```

## 5.3. GitHub Pages
GitHub Pages permite que você publique sites estáticos diretamente do seu repositório GitHub. Para configurar uma página simples:

Crie um arquivo index.md ou index.html na branch gh-pages ou na pasta docs, dependendo da configuração do seu repositório.

Adicione o conteúdo HTML ou Markdown para sua página.

Configure GitHub Pages:

No GitHub, vá até as configurações do repositório.
Na aba "Pages", escolha a branch ou a pasta (por exemplo, gh-pages ou docs) para publicar.

Acesse seu site:

Após a configuração, o GitHub Pages fornecerá um link para o seu site publicado.

