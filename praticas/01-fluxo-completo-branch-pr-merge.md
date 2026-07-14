# Prática 01 - Fluxo completo: branch, commits, PR e merge

## Objetivo

Demonstrar o fluxo completo de trabalho com Git e GitHub:

```text
criar branch -> alterar arquivo -> fazer commit -> push -> abrir PR -> fazer merge
```

---

## Pré-requisitos

- Ter o repositório clonado na máquina.
- Ter acesso ao repositório no GitHub.
- Estar na branch `main`.

Verifique:

```bash
git status
git branch
```

---

## Passo 1 - Atualizar a branch principal

```bash
git switch main
git pull
```

---

## Passo 2 - Criar uma branch

```bash
git switch -c docs/pratica-fluxo-completo
```

---

## Passo 3 - Criar ou alterar um arquivo

Exemplo: crie um arquivo chamado `anotacoes-pratica.md` ou edite algum arquivo da pasta `docs`.

Sugestão de conteúdo:

```md
# Anotações da prática

Nesta prática, criei uma branch, fiz commits, abri um Pull Request e realizei o merge.
```

---

## Passo 4 - Verificar alterações

```bash
git status
```

---

## Passo 5 - Adicionar arquivos

```bash
git add .
```

---

## Passo 6 - Criar commit

```bash
git commit -m "docs: adiciona anotacoes da pratica de pr"
```

---

## Passo 7 - Enviar branch para o GitHub

```bash
git push -u origin docs/pratica-fluxo-completo
```

---

## Passo 8 - Abrir Pull Request

No GitHub:

1. Acesse o repositório.
2. Clique em **Compare & pull request**.
3. Escreva um título claro.
4. Descreva o que foi alterado.
5. Clique em **Create pull request**.

Título sugerido:

```text
docs: adiciona anotacoes da pratica de PR
```

Descrição sugerida:

```md
## O que foi feito

- Criei uma branch de documentação.
- Adicionei anotações da prática.
- Registrei o fluxo completo de PR.

## Como revisar

- Conferir o arquivo alterado.
- Validar se o passo a passo está claro.
```

---

## Passo 9 - Fazer merge

Depois de revisar o PR:

1. Clique em **Merge pull request**.
2. Confirme o merge.
3. Apague a branch pelo GitHub, se desejar.

---

## Passo 10 - Atualizar o repositório local

```bash
git switch main
git pull
git branch -d docs/pratica-fluxo-completo
```

---

## Resultado esperado

Ao final, a alteração criada na branch deve estar integrada na branch `main`.

---

## Checklist da prática

- [ ] Branch criada.
- [ ] Arquivo alterado.
- [ ] Commit criado.
- [ ] Branch enviada para o GitHub.
- [ ] Pull Request aberto.
- [ ] Pull Request revisado.
- [ ] Merge realizado.
- [ ] Branch local removida.
