# Branch

## O que é uma branch?

Uma branch é uma linha independente de desenvolvimento dentro de um repositório Git.

Ela permite criar alterações sem mexer diretamente na branch principal do projeto, que normalmente se chama `main` ou `master`.

Branches são muito usadas para:

- Desenvolver novas funcionalidades;
- Corrigir bugs;
- Fazer testes;
- Escrever documentação;
- Organizar o trabalho em equipe.

---

## Por que usar branches?

Usar branches ajuda a manter o projeto principal estável enquanto novas mudanças estão sendo feitas.

Exemplo:

```text
main
 |
 |--- docs/branch
 |--- feat/login
 |--- fix/menu
```

Cada branch pode ter seus próprios commits. Depois, as alterações podem ser integradas de volta na branch principal usando merge ou Pull Request.

---

## Comandos principais

Listar branches:

```bash
git branch
```

Criar uma branch:

```bash
git branch nome-da-branch
```

Trocar para uma branch:

```bash
git switch nome-da-branch
```

Criar e trocar para uma branch ao mesmo tempo:

```bash
git switch -c nome-da-branch
```

Enviar uma branch para o GitHub:

```bash
git push -u origin nome-da-branch
```

Excluir uma branch local depois do merge:

```bash
git branch -d nome-da-branch
```

---

## Padrões de nomes

Alguns padrões comuns:

```text
docs/branch
docs/comandos-basicos
feat/cadastro-usuario
fix/correcao-menu
chore/organiza-repositorio
```

Prefixos comuns:

| Prefixo | Uso |
| --- | --- |
| `docs/` | Documentação |
| `feat/` | Nova funcionalidade |
| `fix/` | Correção |
| `chore/` | Organização ou manutenção |
| `test/` | Testes |

---

## Exemplo prático

```bash
git switch -c docs/branch
```

Depois de editar os arquivos:

```bash
git status
git add docs/04-branch.md
git commit -m "docs(branch): adiciona anotacoes sobre branches"
git push -u origin docs/branch
```

---

## Resumo

Branch é uma forma de trabalhar em uma alteração separada da linha principal do projeto. Ela deixa o desenvolvimento mais organizado, seguro e colaborativo.

---

## Próximo tópico

[05 - Merge](05-merge.md)
