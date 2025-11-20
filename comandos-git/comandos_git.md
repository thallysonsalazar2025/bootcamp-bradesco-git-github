# 📘 Comandos Essenciais e Avançados do Git

Este arquivo reúne os principais comandos do Git, com **descrição**,
**quando usar** e **como usar** --- ideal para consultas rápidas no dia
a dia do desenvolvimento.

------------------------------------------------------------------------

## 🧩 1. Inicialização

### **git init**

-   **O que faz:** Cria um novo repositório Git.
-   **Quando usar:** Quando você quer começar a versionar um projeto
    local.
-   **Como usar:**

    ```
    git init
    ```

------------------------------------------------------------------------

## 🧩 2. Status e Informações

### **git status**

-   **O que faz:** Mostra arquivos modificados, rastreados, não
    rastreados e pendentes de commit.
-   **Quando usar:** Sempre antes de fazer `add` ou `commit` para saber
    o estado do repositório.
-   **Como usar:**

    ```
    git status
    ```

------------------------------------------------------------------------

## 🧩 3. Adicionar Arquivos ao Staging

### **git add**

-   **O que faz:** Envia arquivos modificados para a área de staging.
-   **Quando usar:** Antes de realizar um commit.
-   **Como usar:**

    ```
    git add nome_do_arquivo
    git add .   # adiciona tudo
    ```

------------------------------------------------------------------------

## 🧩 4. Criar um Commit

### **git commit -m**

-   **O que faz:** Salva as modificações no histórico do repositório.
-   **Quando usar:** Após adicionar conteúdos ao staging.
-   **Como usar:**

    ```
    git commit -m "Descrição clara do que mudou"
    ```

------------------------------------------------------------------------

## 🧩 5. Histórico

### **git log**

-   **O que faz:** Lista os commits realizados.
-   **Quando usar:** Para verificar histórico ou buscar commits antigos.
-   **Como usar:**

    ```
    git log
    ```

------------------------------------------------------------------------

## 🧩 6. Comparações

### **git diff**

-   **O que faz:** Mostra diferenças entre arquivos modificados.
-   **Quando usar:** Antes de fazer um commit para revisar alterações.
-   **Como usar:**

    ```
    git diff
    ```

------------------------------------------------------------------------

## 🧩 7. Repositórios Remotos

### **git remote add origin**

-   **O que faz:** Conecta o repositório local a um repositório remoto.
-   **Quando usar:** No primeiro push para o GitHub.
-   **Como usar:**

    ```
    git remote add origin [https://github.com/usuario/repositorio.git](https://github.com/usuario/repositorio.git)
    ```

------------------------------------------------------------------------

### **git push**

-   **O que faz:** Envia commits locais para o repositório remoto.
-   **Quando usar:** Para atualizar o GitHub com mudanças locais.
-   **Como usar:**

    ```
    git push -u origin main
    ```

------------------------------------------------------------------------

### **git pull**

-   **O que faz:** Baixa e integra alterações do servidor.
-   **Quando usar:** Antes de iniciar novos trabalhos ou atualizar sua
    branch.
-   **Como usar:**

    ```
    git pull
    ```

------------------------------------------------------------------------

### **git clone**

-   **O que faz:** Baixa um repositório remoto para sua máquina.
-   **Quando usar:** Quando quiser copiar um projeto existente.
-   **Como usar:**

    ```
    git clone [https://github.com/usuario/repositorio.git](https://github.com/usuario/repositorio.git)
    ```

------------------------------------------------------------------------

## 🧩 8. Branches

### **git branch**

-   **O que faz:** Lista ou cria branches.
-   **Quando usar:** Para organizar versões paralelas do projeto.
-   **Como usar:**

    ```
    git branch             # lista
    git branch nova-branch # cria
    ```

### **git checkout**

-   **O que faz:** Troca de branch.
-   **Quando usar:** Quando quiser trabalhar em outra linha de
    desenvolvimento.
-   **Como usar:**

    ```
    git checkout nome-da-branch
    ```
    

### **git switch**

-   **O que faz:** Troca de branch de forma moderna e intuitiva (substituto do `git checkout` para trocar de branch).
-   **Quando usar:** Para mudar de branch de forma clara, ou criar e trocar de branch com um único comando.
-   **Como usar:**

    ```
    git switch nome-da-branch
    git switch -c nova-branch # cria e troca
    ```

### **git merge**

-   **O que faz:** Junta duas branches.
-   **Quando usar:** Quando uma feature está pronta e deve ir para a
    branch principal.
-   **Como usar:**

    ```
    git merge nome-da-branch
    ```

------------------------------------------------------------------------

## 🧩 9. Desfazer Ações

### **git restore**

-   **O que faz:** Restaura arquivos modificados para estado anterior (remove alterações do *working directory* ou do *staging area*).
-   **Quando usar:** Para descartar mudanças locais não *comitadas*.
-   **Como usar:**

    ```
    git restore nome_do_arquivo
    git restore --staged nome_do_arquivo # remove do staging
    ```

### **git reset**

-   **O que faz:** Remove arquivos do staging ou desfaz commits (move o `HEAD`).
-   **Quando usar:** Para corrigir erros no staging ou desfazer *commits* locais, com cautela.
-   **Como usar:**

    ```
    git reset nome_do_arquivo
    git reset --soft HEAD~1   # desfaz 1 commit, mantendo as mudanças no staging
    git reset --hard HEAD~1   # desfaz 1 commit, descartando TODAS as mudanças
    ```

------------------------------------------------------------------------

## 🧩 10. Atualizar Informações do Repositório Remoto

### **git fetch**

-   **O que faz:** Baixa dados do remoto (como novas *branches* e *commits*) sem integrar/aplicar ao seu *working directory*.
-   **Quando usar:** Para analisar mudanças no servidor antes de dar um `git pull` ou `git merge`.
-   **Como usar:**

    ```
    git fetch
    ```

------------------------------------------------------------------------

## 🚀 11. Comandos Avançados

Estes comandos são usados para **reescrever o histórico**, **transferir *commits*** entre branches ou **inspecionar** o repositório em profundidade.

### **git rebase**

-   **O que faz:** Move ou combina uma sequência de *commits* para uma nova base (reorganiza o histórico de *commits*).
-   **Quando usar:** Para **integrar mudanças** de uma *branch* principal (ex: `main`) na sua *feature branch*, mantendo o histórico de *commits* linear e limpo.
-   **Como usar:**

    ```
    git rebase main # Reorganiza a branch atual sobre a última versão da 'main'
    ```

### **git rebase -i**

-   **O que faz:** Inicia um **rebase interativo**. Permite reordenar, editar, agrupar (squash), ou excluir *commits* dentro de um intervalo.
-   **Quando usar:** Para **limpar e simplificar** o histórico de uma *feature branch* (transformar 5 *commits* pequenos em 1 coeso) antes de abri-la para *merge*.
-   **Como usar:**

    ```
    git rebase -i HEAD~3 # Abre o modo interativo para os últimos 3 commits
    ```

### **git cherry-pick**

-   **O que faz:** Aplica as mudanças introduzidas por um **único *commit*** em uma *branch* diferente.
-   **Quando usar:** Para aplicar um *bugfix* específico ou uma pequena *feature* de uma *branch* em outra, sem mesclar toda a *branch*.
-   **Como usar:**

    ```
    git cherry-pick <commit-hash>
    ```

### **git stash**

-   **O que faz:** Salva temporariamente o estado atual do *working directory* e *staging area* (trabalho não *comitado*), permitindo que você mude de *branch*.
-   **Quando usar:** Quando você precisa **mudar rapidamente de *branch*** para resolver um *hotfix* ou testar algo, mas não está pronto para fazer *commit* do trabalho atual.
-   **Como usar:**

    ```
    git stash       # Salva o trabalho atual
    git stash pop   # Aplica o último stash e o remove da lista
    ```

### **git revert**

-   **O que faz:** Cria um **novo *commit*** que **desfaz as mudanças** introduzidas por um *commit* anterior. Não reescreve o histórico.
-   **Quando usar:** Para desfazer um *commit* que **já foi enviado** (`pushed`) para um repositório compartilhado, pois é a maneira segura de desfazer mudanças em histórico público.
-   **Como usar:**

    ```
    git revert <commit-hash>
    ```

### **git reflog**

-   **O que faz:** Mostra um log (registro) de todas as **ações que atualizaram o `HEAD`** do seu repositório (ex: *checkouts*, *commits*, *resets*).
-   **Quando usar:** Se você **"perdeu" um *commit*** após um `reset --hard` ou um `rebase` errado. Permite encontrar o *hash* do estado perdido para restaurá-lo.
-   **Como usar:**

    ```
    git reflog
    ```

### **git commit --amend**

-   **O que faz:** Substitui o último *commit* pelo novo conteúdo *staged* e/ou permite reescrever a mensagem do último *commit*.
-   **Quando usar:** Para corrigir um **erro rápido** (typo) ou **esquecer um arquivo** no *commit* mais recente, antes de enviá-lo ao servidor.
-   **Como usar:**

    ```
    git commit --amend --no-edit # Adiciona o staged sem mudar a mensagem
    git commit --amend -m "Nova Mensagem"
    ```
