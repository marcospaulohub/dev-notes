# 🌀 Guia Rápido de Comandos Git

Este documento contém comandos Git essenciais para gerenciamento de projetos.

## 1. Inicialização do Projeto
*   `git init`: Inicializa um novo repositório Git no diretório atual.
*   `git clone [URL]`: Clona um repositório existente para o seu computador.
*   `git remote add origin [URL]`: Adiciona um repositório remoto, geralmente um link do GitHub ou GitLab [14].

## 2. Gerenciamento de Arquivos
*   `git status`: Verifica o status dos arquivos do repositório (modificados, novos, etc.).
*   `git add [arquivo]`: Adiciona arquivos à área de "staging" (preparo) para a próxima confirmação [2].
    *   `git add .`: Adiciona todas as alterações no diretório.
*   `git rm [arquivo]`: Remove um arquivo do repositório [2].
*   `git mv [arquivo_antigo] [arquivo_novo]`: Renomeia um arquivo [3].

## 3. Confirmação de Alterações
*   `git commit -m "Sua mensagem aqui"`: Confirma as alterações preparadas com uma mensagem descritiva [7].
*   `git commit -am "Sua mensagem aqui"`: Adiciona e confirma todas as alterações em um único passo (para arquivos que já foram monitorados) [7].
*   `git commit --amend -m "Nova mensagem"`: Altera a mensagem do último commit [7].

## 4. Branches (Ramos)
*   `git branch`: Lista todos os branches.
*   `git branch [nome-do-branch]`: Cria um novo branch [6].
*   `git checkout [nome-do-branch]`: Muda para outro branch [13].
*   `git checkout -b [nome-do-branch]`: Cria e muda para um novo branch ao mesmo tempo [14].

## 5. Compartilhamento e Sincronização
*   `git push`: Envia as alterações para o repositório remoto [13].
*   `git pull`: Puxa as alterações mais recentes do repositório remoto [13].
*   `git log`: Exibe o histórico de commits.

## 6. Detalhes e Comparação
*   `git diff`: Mostra as diferenças entre a área de trabalho e o "staging" [12].
*   `git diff --staged`: Mostra as diferenças entre o "staging" e o último commit [12].
*   `git diff [commit1] [commit2]`: Mostra as diferenças entre dois commits específicos.
