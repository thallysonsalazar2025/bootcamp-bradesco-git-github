# 📘 Comandos Essenciais do Git

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

```{=html}
<!-- -->
```
    git init

------------------------------------------------------------------------

## 🧩 2. Status e Informações

### **git status**

-   **O que faz:** Mostra arquivos modificados, rastreados, não
    rastreados e pendentes de commit.
-   **Quando usar:** Sempre antes de fazer `add` ou `commit` para saber
    o estado do repositório.
-   **Como usar:**

```{=html}
<!-- -->
```
    git status

------------------------------------------------------------------------

## 🧩 3. Adicionar Arquivos ao Staging

### **git add**

-   **O que faz:** Envia arquivos modificados para a área de staging.
-   **Quando usar:** Antes de realizar um commit.
-   **Como usar:**

```{=html}
<!-- -->
```
    git add nome_do_arquivo
    git add .   # adiciona tudo

------------------------------------------------------------------------

## 🧩 4. Criar um Commit

### **git commit -m**

-   **O que faz:** Salva as modificações no histórico do repositório.
-   **Quando usar:** Após adicionar conteúdos ao staging.
-   **Como usar:**

```{=html}
<!-- -->
```
    git commit -m "Descrição clara do que mudou"

------------------------------------------------------------------------

## 🧩 5. Histórico

### **git log**

-   **O que faz:** Lista os commits realizados.
-   **Quando usar:** Para verificar histórico ou buscar commits antigos.
-   **Como usar:**

```{=html}
<!-- -->
```
    git log

------------------------------------------------------------------------

## 🧩 6. Comparações

### **git diff**

-   **O que faz:** Mostra diferenças entre arquivos modificados.
-   **Quando usar:** Antes de fazer um commit para revisar alterações.
-   **Como usar:**

```{=html}
<!-- -->
```
    git diff

------------------------------------------------------------------------

## 🧩 7. Repositórios Remotos

### **git remote add origin**

-   **O que faz:** Conecta o repositório local a um repositório remoto.
-   **Quando usar:** No primeiro push para o GitHub.
-   **Como usar:**

```{=html}
<!-- -->
```
    git remote add origin https://github.com/usuario/repositorio.git

------------------------------------------------------------------------

### **git push**

-   **O que faz:** Envia commits locais para o repositório remoto.
-   **Quando usar:** Para atualizar o GitHub com mudanças locais.
-   **Como usar:**

```{=html}
<!-- -->
```
    git push -u origin main

------------------------------------------------------------------------

### **git pull**

-   **O que faz:** Baixa e integra alterações do servidor.
-   **Quando usar:** Antes de iniciar novos trabalhos ou atualizar sua
    branch.
-   **Como usar:**

```{=html}
<!-- -->
```
    git pull

------------------------------------------------------------------------

### **git clone**

-   **O que faz:** Baixa um repositório remoto para sua máquina.
-   **Quando usar:** Quando quiser copiar um projeto existente.
-   **Como usar:**

```{=html}
<!-- -->
```
    git clone https://github.com/usuario/repositorio.git

------------------------------------------------------------------------

## 🧩 8. Branches

### **git branch**

-   **O que faz:** Lista ou cria branches.
-   **Quando usar:** Para organizar versões paralelas do projeto.
-   **Como usar:**

```{=html}
<!-- -->
```
    git branch             # lista
    git branch nova-branch # cria

### **git checkout**

-   **O que faz:** Troca de branch.
-   **Quando usar:** Quando quiser trabalhar em outra linha de
    desenvolvimento.
-   **Como usar:**

```{=html}
<!-- -->
```
    git checkout nome-da-branch

### **git switch**

-   **O que faz:** Troca de branch de forma moderna e intuitiva.
-   **Como usar:**

```{=html}
<!-- -->
```
    git switch nome-da-branch

### **git merge**

-   **O que faz:** Junta duas branches.
-   **Quando usar:** Quando uma feature está pronta e deve ir para a
    branch principal.
-   **Como usar:**

```{=html}
<!-- -->
```
    git merge nome-da-branch

------------------------------------------------------------------------

## 🧩 9. Desfazer Ações

### **git restore**

-   **O que faz:** Restaura arquivos modificados para estado anterior.
-   **Como usar:**

```{=html}
<!-- -->
```
    git restore nome_do_arquivo

### **git reset**

-   **O que faz:** Remove arquivos do staging ou desfaz commits.
-   **Quando usar:** Para corrigir erros, com cautela.
-   **Como usar:**

```{=html}
<!-- -->
```
    git reset nome_do_arquivo
    git reset --soft HEAD~1
    git reset --hard HEAD~1

------------------------------------------------------------------------

## 🧩 10. Atualizar Informações do Repositório Remoto

### **git fetch**

-   **O que faz:** Baixa dados do remoto sem integrar.
-   **Quando usar:** Para analisar mudanças antes de aplicar.
-   **Como usar:**

```{=html}
<!-- -->
```
    git fetch
