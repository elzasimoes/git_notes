# Comandos Git Diários

## `git status`
- Verifica o status atual do repositório, mostrando quais arquivos foram modificados, adicionados ou removidos.

## `git add <arquivo>`
- Adiciona mudanças em arquivos específicos ao índice (stage) para serem incluídas no próximo commit.

## `git commit -m "mensagem"`
- Cria um novo commit com as mudanças que foram adicionadas ao índice, incluindo uma mensagem descritiva.

## `git pull`
- Atualiza o repositório local com as mudanças da branch remota, unindo-as com as alterações locais.

## `git push`
- Envia os commits locais para o repositório remoto, tornando as mudanças acessíveis a outros desenvolvedores.

## `git branch`
- Lista as branches locais ou cria novas branches.

## `git checkout <branch>`
- Troca de branch ou restaura arquivos do índice para o diretório de trabalho.

## `git merge <branch>`
- Mescla uma branch com outra, integrando as mudanças. Cria um merge commit.

## `git log`
- Mostra o histórico de commits do repositório.

## `git diff`
- Exibe as diferenças entre commits, branches, ou arquivos.

## `git stash`
- Salva temporariamente as mudanças locais que ainda não foram commitadas, limpando-as do diretório de trabalho.

## `git stash pop`
- Restaura as mudanças previamente armazenadas com `git stash` e remove a stash do histórico.

## `git stash list`
- Lista as stashes guardadas.

## `git stash clear`
- Limpa todas as stashes armazenadas.

## `git stash push -m "mensagem"`
- Salva as mudanças locais com uma mensagem descritiva.

## `git reset --hard <commit>`
- Restaura o repositório para um estado anterior, descartando mudanças e commits após o commit especificado.

## `git rebase <branch>`
- Reaplica commits em cima de outro branch para manter um histórico linear.

## `git restore <arquivo>`
- Restaura o estado de um arquivo específico ao último commit, descartando as mudanças feitas localmente.

## `git restore --source=<commit> <arquivo>`
- Restaura o estado de um arquivo específico a partir de um commit especificado. Exemplo:

  ```
  git restore --source=5081a55bc92af2917c8519f16a7412b86ba3b1c2 index.html
  ```

### Diferença entre `merge` e `rebase`
- O `merge` junta o trabalho de duas branches, podendo gerar um merge commit.
- O `rebase` aplica os commits de outra branch na branch atual, mantendo um histórico linear.
