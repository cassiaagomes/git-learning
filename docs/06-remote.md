# Remote

## O que é remote?

Remote é o nome dado a um repositório remoto conectado ao seu repositório local.

O remote mais comum se chama `origin`. Ele normalmente aponta para o repositório no GitHub, GitLab ou outra plataforma.

---

## Para que serve?

O remote permite sincronizar o trabalho local com o repositório hospedado na nuvem.

Com ele, é possível:

- Baixar alterações feitas por outras pessoas;
- Enviar commits locais para o GitHub;
- Criar branches remotas;
- Trabalhar em equipe;
- Manter backup do projeto.

---

## Ver remotes configurados

```bash
git remote -v
```

Exemplo de saída:

```text
origin  https://github.com/usuario/projeto.git (fetch)
origin  https://github.com/usuario/projeto.git (push)
```

---

## Adicionar um remote

```bash
git remote add origin https://github.com/usuario/projeto.git
```

---

## Alterar a URL do remote

```bash
git remote set-url origin https://github.com/usuario/novo-projeto.git
```

---

## Remover um remote

```bash
git remote remove origin
```

---

## Remote x branch remota

O remote é a conexão com o repositório hospedado.

A branch remota é uma referência para uma branch que existe nesse repositório remoto.

Exemplo:

```text
origin/main
origin/docs/branch
origin/feat/login
```

---

## Resumo

Remote é a ponte entre o repositório local e o repositório na nuvem. Com ele, usamos comandos como `push`, `pull` e `fetch`.

---

## Próximo tópico

[07 - Comandos básicos](07-comandos-basicos.md)
