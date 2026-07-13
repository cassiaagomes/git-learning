# Merge

## O que é merge?

Merge é o processo de juntar alterações de uma branch em outra.

Um exemplo comum é criar uma branch para documentação, fazer commits nela e depois integrar essas alterações na branch `main`.

---

## Quando usar merge?

Use merge quando uma alteração já estiver pronta para entrar em outra branch.

Exemplos:

- Uma documentação foi finalizada.
- Uma correção foi testada.
- Uma funcionalidade foi revisada.
- Um Pull Request foi aprovado.

---

## Exemplo básico

Imagine que existe uma branch chamada `docs/branch` com alterações prontas.

Primeiro, volte para a branch principal:

```bash
git switch main
```

Atualize a branch principal:

```bash
git pull
```

Faça o merge:

```bash
git merge docs/branch
```

Se tudo estiver certo, envie a `main` atualizada:

```bash
git push
```

---

## Tipos comuns de merge

### Fast-forward

Acontece quando a branch principal não teve novos commits desde que a outra branch foi criada. O Git apenas avança o ponteiro da branch.

### Merge commit

Acontece quando as duas branches possuem históricos diferentes. O Git cria um commit extra para registrar a junção.

### Squash merge

Muito usado em Pull Requests. Junta todos os commits da branch em um único commit na branch principal.

---

## Merge pelo GitHub

No GitHub, o merge normalmente acontece por meio de um Pull Request.

Fluxo:

```text
criar branch -> fazer commits -> push -> abrir PR -> revisar -> merge
```

---

## Resumo

Merge é a integração de alterações entre branches. Ele é essencial para juntar trabalhos feitos separadamente e manter o histórico do projeto organizado.

---

## Próximo tópico

[06 - Remote](06-remote.md)
