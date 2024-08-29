# 4. Resolvendo Conflitos e Melhorando o Fluxo de Trabalho

## 4.1. Conflitos de Merge
Conflitos de *merge* ocorrem quando duas pessoas modificam a mesma parte de um arquivo em diferentes branches, e o Git não sabe qual versão manter. Para resolver um conflito:

1. O Git marca as áreas do arquivo em conflito assim:
   ```plaintext
   <<<<<<< HEAD
   Seu código atual aqui
   =======
   O código do outro branch aqui
   >>>>>>> branch-em-conflito
```

2. Edite o arquivo para escolher qual código deve permanecer (ou combine os dois).

3. Após resolver os conflitos, adicione as mudanças:

```bash
git add nome-do-arquivo
````

4. Finalize o merge:

```bash
git commit
```

## 4.2. Rebasing

O rebase é uma maneira de aplicar as mudanças de uma branch em cima de outra, criando um histórico linear e mais limpo. Diferente do merge, que cria um novo commit para combinar duas branches, o rebase move a branch atual para o topo de outra. Para fazer um rebase:

1. Primeiro, vá para a branch que deseja rebasear:

```bash
git checkout minha-branch
```
2. Em seguida, faça o rebase:

```bash
git rebase main
```

2. Resolva quaisquer conflitos que possam surgir, da mesma maneira que faria em um merge, e depois continue:

```bash
git rebase --continue
```

## 4.3. Git Stash

O stash é útil quando você precisa mudar de branch rapidamente, mas ainda tem alterações não commitadas. Ele salva temporariamente suas mudanças sem fazer um commit. Para usar o stash:

1. Para guardar suas mudanças:

```bash
git stash
```

2. Para ver a lista de stashes guardados:

```bash
git stash list
```

3. Para aplicar o último stash guardado:

```bash
git stash apply
```

4. Para aplicar e remover o stash:

```bash
git stash pop
```

Essas ferramentas ajudam a manter um fluxo de trabalho eficiente e a resolver problemas comuns que surgem durante a colaboração em projetos. Agora, você está pronto para lidar com situações mais complexas no Git!


