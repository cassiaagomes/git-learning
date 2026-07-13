# Boas práticas

## Por que boas práticas importam?

Boas práticas deixam o histórico do projeto mais fácil de entender, revisar e manter.

Um bom histórico ajuda a responder perguntas como:

- O que mudou?
- Por que mudou?
- Quando mudou?
- Quem fez a alteração?
- Qual commit introduziu determinado comportamento?

---

## Commits pequenos e atômicos

Um commit atômico registra uma alteração focada em um único objetivo.

Bom exemplo:

```text
docs(branch): adiciona explicacao sobre criacao de branches
```

Exemplo menos ideal:

```text
altera um monte de coisa
```

---

## Mensagens claras

Uma boa mensagem de commit deve ser objetiva e explicar a intenção da mudança.

Estrutura recomendada:

```text
tipo(escopo): descricao curta no imperativo ou presente
```

Exemplos:

```text
docs(remote): explica uso do origin
fix(readme): corrige link quebrado
chore(repo): organiza estrutura de pastas
```

---

## Revise antes de commitar

Antes de criar o commit, confira:

```bash
git status
git diff
```

Para revisar o que já foi para a Staging Area:

```bash
git diff --staged
```

---

## Use branches para organizar o trabalho

Evite trabalhar direto na `main` quando estiver praticando fluxos colaborativos.

Prefira:

```bash
git switch -c docs/novo-topico
```

---

## Mantenha o README atualizado

O `README.md` deve explicar o objetivo do projeto e apontar para os principais arquivos.

Ele funciona como a porta de entrada do repositório.

---

## Use `.gitignore`

O `.gitignore` evita versionar arquivos desnecessários, como:

- Dependências instaladas;
- Arquivos temporários;
- Logs;
- Configurações locais;
- Pastas de build.

---

## Checklist antes do push

- [ ] Estou na branch correta?
- [ ] Rodei `git status`?
- [ ] Adicionei apenas os arquivos necessários?
- [ ] A mensagem do commit está clara?
- [ ] Minha branch está atualizada com a `main`?
- [ ] O PR explica bem a mudança?

---

## Resumo

Boas práticas tornam o trabalho com Git mais organizado. O foco é manter commits pequenos, mensagens claras, branches bem nomeadas e Pull Requests fáceis de revisar.
