
# Resumo do Curso de Git e GitHub

## 01. Analisando Mudanças com Git
Nesta seção, você aprende a analisar mudanças no código usando o Git. Aqui estão alguns dos comandos principais:

- **`git diff`**: Compara as diferenças entre o conteúdo do seu diretório de trabalho e o que está indexado, ou entre dois commits específicos. Exemplo:
  ```bash
  git diff HEAD~1 HEAD
  ```
  Isso compara o commit atual com o commit anterior.

- **`git log`**: Exibe o histórico de commits. Você pode usar opções como `--oneline` para um resumo mais compacto ou `--stat` para ver as mudanças em cada arquivo. Exemplo:
  ```bash
  git log --oneline --stat
  ```

- **`git blame`**: Mostra a última modificação de cada linha em um arquivo, útil para identificar quem fez o quê e quando. Exemplo:
  ```bash
  git blame nome_do_arquivo
  ```

## 02. Organizando o Trabalho
Organizar o trabalho de forma eficiente é crucial, e o Git oferece diversas ferramentas para isso:

- **`git branch`**: Gerencia branches no seu repositório. Você pode listar, criar ou deletar branches. Exemplo:
  ```bash
  git branch nome_da_branch
  ```
  Isso cria uma nova branch chamada `nome_da_branch`.

- **`git checkout`**: Usado para mudar de branch ou restaurar arquivos. Para mudar de branch:
  ```bash
  git checkout nome_da_branch
  ```
  Ou para criar e mudar para uma nova branch:
  ```bash
  git checkout -b nova_branch
  ```

- **`git merge`**: Combina o conteúdo de diferentes branches. Exemplo:
  ```bash
  git merge nome_da_branch
  ```

- **`git rebase`**: Reaplica commits de uma branch em cima de outra, útil para manter um histórico linear. Exemplo:
  ```bash
  git rebase main
  ```

## 03. Manipulando Versões
Manipular versões é essencial para o gerenciamento de projetos:

- **`git reset`**: Move o ponteiro HEAD e altera o estado do diretório de trabalho. Pode ser usado para desfazer commits:
  ```bash
  git reset --soft HEAD~1
  ```
  Isso desfaz o último commit, mas mantém as mudanças no diretório de trabalho.

- **`git checkout`**: Além de mudar de branch, pode ser usado para restaurar arquivos de versões anteriores:
  ```bash
  git checkout HEAD~1 -- nome_do_arquivo
  ```

- **`git revert`**: Cria um novo commit que desfaz mudanças de commits anteriores:
  ```bash
  git revert HEAD
  ```
  Isso cria um commit que reverte o último commit.

- **`git tag`**: Marca commits importantes com um nome amigável:
  ```bash
  git tag -a v1.0 -m "Versão 1.0"
  ```

## 04. Gerando Entregas
Preparar o código para entrega é uma parte crucial do desenvolvimento:

- **`git tag`**: Como mencionado, tags são usadas para marcar pontos específicos no histórico, como releases:
  ```bash
  git tag -a v1.0 -m "Versão 1.0"
  ```

- **`git archive`**: Cria um arquivo compactado do conteúdo do repositório, ideal para entregar código:
  ```bash
  git archive --format=zip --output=saida.zip HEAD
  ```

- **`git push`**: Envia commits e tags para o repositório remoto. Para enviar tags:
  ```bash
  git push origin --tags
  ```

## 05. Controle sobre os Commits
O controle sobre os commits permite um histórico mais limpo e compreensível:

- **`git rebase -i`**: Permite reescrever o histórico de commits de forma interativa, para combinar ou editar commits:
  ```bash
  git rebase -i HEAD~3
  ```
  Isso inicia um rebase interativo nos últimos 3 commits.

- **`git commit --amend`**: Modifica o último commit, útil para corrigir mensagens de commit ou adicionar mudanças:
  ```bash
  git commit --amend -m "Nova mensagem de commit"
  ```

- **`git cherry-pick`**: Aplica um commit específico de outra branch ao seu branch atual:
  ```bash
  git cherry-pick abc1234
  ```
  Isso aplica o commit `abc1234` ao seu branch atual.
