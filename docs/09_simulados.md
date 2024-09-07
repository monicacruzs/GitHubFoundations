# Simulados e Cenários Práticos

## 1. Perguntas e Respostas

### Fundamentos do Git

1. **O que é Git?** Explique brevemente.  
   **Resposta:** Git é um sistema de controle de versão distribuído que permite que vários desenvolvedores trabalhem no mesmo projeto sem sobrescrever o trabalho uns dos outros.

2. **Qual comando é usado para inicializar um repositório Git?**
   - A) `git start`
   - B) `git init`
   - C) `git clone`
   - D) `git create`

   **Resposta Correta:** B

3. **Como fazer um commit em Git?**  
   **Resposta:** `git commit -m "Mensagem do commit"`

4. **Qual comando é usado para enviar alterações locais para o repositório remoto?**
   - A) `git pull`
   - B) `git push`
   - C) `git clone`
   - D) `git merge`

   **Resposta Correta:** B

5. **Como você faz para clonar um repositório existente do GitHub para seu computador?**
   - A) `git pull <url-do-repositorio>`
   - B) `git copy <url-do-repositorio>`
   - C) `git clone <url-do-repositorio>`
   - D) `git checkout <url-do-repositorio>`

   **Resposta Correta:** C

6. **Qual é o processo recomendado para contribuir com um repositório público no GitHub, ao qual você não tem permissão de escrita?**
   - A) Clone o repositório, faça alterações, e envie um push diretamente para a branch `main`.
   - B) Crie um fork do repositório, faça suas alterações em uma branch separada no fork, e abra um pull request para o repositório original.
   - C) Solicite permissões de escrita ao dono do repositório, e então faça suas alterações.
   - D) Faça o download dos arquivos manualmente, edite localmente e envie por e-mail as alterações ao administrador do repositório.

   **Resposta Correta:** B

7. **O que é um pull request e como ele é usado?**  
   **Resposta:** Um pull request é uma solicitação para integrar mudanças de uma branch em outra, geralmente de um fork para o repositório original. Ele é usado para colaborar em projetos, permitindo que outros revisem e discutam mudanças propostas antes de aceitá-las.

8. **Como resolver conflitos de merge?**  
   **Resposta:** Identifique o conflito, edite os arquivos afetados para resolver as diferenças, adicione as mudanças ao stage com `git add`, e finalize o merge com `git commit`.

9. **Quando é recomendado usar `git rebase` em vez de `git merge`?**  
   **Resposta:** `git rebase` é recomendado quando você quer manter um histórico linear e limpo, aplicando suas mudanças no topo da branch de destino.

10. **Como criar e usar tags no Git?**  
    **Resposta:** Use `git tag -a <nome-da-tag> -m "mensagem"` para criar uma tag anotada, e `git push origin <nome-da-tag>` para enviá-la ao repositório remoto.

11. **O que são submódulos e como usá-los?**  
    **Resposta:** Submódulos são repositórios Git dentro de outros repositórios Git. Eles são usados para gerenciar dependências em projetos que utilizam outros projetos.

12. **Qual é o propósito de usar CodeQL no GitHub?**
    - A) Para executar comandos de linha de comando diretamente no repositório.
    - B) Para proteger o repositório contra acesso não autorizado.
    - C) Para realizar análises de segurança automatizadas e identificar vulnerabilidades no código.
    - D) Para gerar documentação automaticamente.

    **Resposta Correta:** C

13. **Qual comando do GitHub CLI é usado para criar um pull request?**
    - A) `gh pr new`
    - B) `git create pull-request`
    - C) `gh pr create`
    - D) `git request pull`

    **Resposta Correta:** C

14. **Quais práticas são recomendadas para proteger um repositório GitHub de acesso não autorizado?**
    - A) Usar autenticação de dois fatores (2FA).
    - B) Compartilhar senhas de acesso com todos os membros da equipe.
    - C) Tornar o repositório privado e usar permissões granulares para usuários.
    - D) A e C.

    **Resposta Correta:** D

15. **Qual funcionalidade do GitHub permite que você rastreie tarefas e progresso de forma visual através de cartões e colunas?**
    - A) GitHub Actions
    - B) GitHub Discussions
    - C) GitHub Projects
    - D) GitHub Pages
   
    **Resposta Correta:** C
    
17. **Como você configuraria uma pipeline de CI/CD básica usando GitHub Actions para testar automaticamente o código a cada novo commit?**   
    - A) Criar um arquivo .yml em .github/workflows com uma definição de job que inclui etapas de instalação, teste e build.
    - B) Configurar um servidor manualmente para monitorar o repositório e rodar scripts de teste.
    - C) Editar diretamente o código fonte sem nenhum teste.
    - D) Configurar o GitHub Pages para rodar testes.

    **Resposta Correta:** A

18. **Qual das seguintes opções descreve melhor o GitHub Sponsors?**
    - A) Um recurso para automatizar tarefas de desenvolvimento.
    - B) Uma plataforma que permite a desenvolvedores receberem suporte financeiro da comunidade.
    - C) Uma ferramenta para gerenciar branches e pull requests.
    - D) Um recurso para hospedar sites estáticos gratuitamente.

    **Resposta Correta:** B


## 2. Cenários Práticos

### Cenário 1: Trabalhando com Branches

Você está colaborando em um projeto com sua equipe e precisa adicionar uma nova funcionalidade sem afetar o código existente na branch `main`.

1. Crie uma nova branch chamada `feature/nova-funcionalidade`:
   ```bash
   git branch feature/nova-funcionalidade

2. Mude para a nova branch:
   ```bash
   git checkout feature/nova-funcionalidade

3. Implemente a funcionalidade e faça commits das mudanças:

   ```bash
   git add .
   git commit -m "Implementa nova funcionalidade"

4. Una as mudanças de volta à branch main:

   ```bash
   git checkout main
   git merge feature/nova-funcionalidade
   
### Cenário 2: Resolver Conflitos de Merge

Ao tentar fazer merge da branch feature/melhorias-ui com a branch main, você enfrenta um conflito. Pratique as seguintes etapas:

1. Use o merge para tentar fundir as branches:

   ```bash
   git merge feature/melhorias-ui
   
   Identifique e resolva os conflitos manualmente no editor de texto.

2. Adicione os arquivos corrigidos ao stage:

   ```bash
   git add .

3. Complete o merge:

   ```bash
   git commit -m "Resolve conflitos de merge entre melhorias-ui e main"

4. Enviar para o repositório remoto com git push:
   
   ```bash
   git push
   

### Cenário 3: Configuração de Repositórios Remotos

Você está configurando um repositório local para colaborar com sua equipe no GitHub.

1. Adicione um repositório remoto chamado origin:

    ```bash
    git remote add origin https://github.com/usuario/repo.git

2. Verifique a configuração do repositório remoto:

    ```bash
    git remote -v

3. Envie suas mudanças locais para o repositório remoto:

    ```bash
    git push origin main

### Cenário 4: Revertendo Alterações

Você fez um commit que introduziu um bug crítico. Pratique como reverter um commit:

1. Identifique o hash do commit a ser revertido usando:

    ```bash
    git log

2. Revertendo o commit com o comando:

    ```bash
    git revert <hash-do-commit>

3. Confirme a mensagem de commit gerada pelo Git.

### Cenário 5: Configurar um Workflow com GitHub Actions

1. Configure uma pipeline de CI/CD simples que testa automaticamente um projeto Python a cada novo commit:
2. Crie um arquivo .yml em .github/workflows no seu repositório.
3. Configure o workflow para instalar dependências, rodar testes com pytest, e gerar um relatório.
4. Faça commit do workflow e valide se o job é executado corretamente no GitHub Actions.

### Cenário 6: Gerenciar um Repositório com Múltiplas Branches

1. Pratique a criação e o gerenciamento de branches:
2. Crie uma nova branch chamada hotfix/bug-corrigido.
3. Faça algumas mudanças em um arquivo de código e faça commit.
4. Mude para a branch main e traga as alterações da hotfix/bug-corrigido usando git merge.
5. Apague a branch hotfix/bug-corrigido após o merge.

### Cenário 7: Usar git remote para Gerenciar Vários Repositórios

1. Configure um repositório local para ter dois remotes:
2. Crie um repositório no GitHub e um fork desse repositório.
2. Adicione o fork como um segundo remote chamado upstream.
3. Pratique os comandos para buscar e sincronizar alterações entre os dois remotes.


