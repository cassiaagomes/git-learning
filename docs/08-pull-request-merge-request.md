# Pull Request e Merge Request

## O que é Pull Request?

Pull Request, também chamado de PR, é uma solicitação para integrar alterações de uma branch em outra.

No GitHub, o nome usado é **Pull Request**. No GitLab, o nome comum é **Merge Request**. A ideia é a mesma: revisar uma alteração antes de fazer o merge.

---

## Para que serve?

Um Pull Request permite:

- Mostrar quais arquivos foram alterados;
- Explicar o objetivo da mudança;
- Receber comentários e sugestões;
- Rodar verificações automáticas;
- Aprovar e fazer merge com mais segurança.

---

## Fluxo completo

```text
1. Criar uma branch
2. Fazer alterações
3. Criar commits
4. Enviar a branch para o remoto
5. Abrir Pull Request
6. Revisar alterações
7. Resolver comentários ou conflitos
8. Fazer merge na branch principal
```

---

## Exemplo de fluxo na prática

Criar branch:

```bash
git switch -c docs/pull-request
```

Fazer alterações nos arquivos.

Verificar estado:

```bash
git status
```

Adicionar e commitar:

```bash
git add docs/08-pull-request-merge-request.md
git commit -m "docs(pr): adiciona anotacoes sobre pull request"
```

Enviar para o GitHub:

```bash
git push -u origin docs/pull-request
```

Depois disso, abra o GitHub e clique em **Compare & pull request**.

---

## O que escrever em um PR?

Um bom PR deve explicar:

- O que foi feito;
- Por que foi feito;
- Como testar ou revisar;
- Se existe algum ponto de atenção.

Exemplo:

```md
## O que foi feito

- Adiciona documentação sobre Pull Request.
- Explica diferença entre PR e MR.

## Como revisar

- Ler o arquivo docs/08-pull-request-merge-request.md.
- Conferir se o fluxo está claro.
```

---

## Após o merge

Depois que o PR for integrado:

```bash
git switch main
git pull
git branch -d docs/pull-request
```

Se quiser apagar a branch remota, isso pode ser feito pelo GitHub ou com:

```bash
git push origin --delete docs/pull-request
```

---

## Resumo

Pull Request e Merge Request são formas organizadas de revisar e integrar alterações. Esse fluxo é essencial para colaboração em projetos reais.

---

## Próximo tópico

[09 - Conflitos de merge](09-conflitos-de-merge.md)
