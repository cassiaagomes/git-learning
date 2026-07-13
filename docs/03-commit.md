# Commit

## O que é um commit?

Um commit representa um registro permanente das alterações realizadas em um projeto.

Sempre que um commit é criado, o Git salva um "snapshot" (estado atual) dos arquivos versionados, permitindo que essas alterações sejam recuperadas no futuro.

Cada commit possui um identificador único (hash), além de informações como autor, data, horário e uma mensagem descritiva.

---

## Como funciona um commit?

Antes de criar um commit, as alterações passam por uma área chamada **Staging Area**.

O fluxo é o seguinte:

```
Working Directory
        │
        ▼
git add
        │
        ▼
Staging Area
        │
        ▼
git commit
        │
        ▼
Histórico do Git
```

---

## Criando um commit

Primeiro adicionamos os arquivos:

```bash
git add .
```

Depois registramos as alterações:

```bash
git commit -m "docs(commit): adiciona documentação sobre commits"
```

---

## Visualizando o histórico

Para listar os commits realizados:

```bash
git log
```

Ou de forma resumida:

```bash
git log --oneline
```

---

## Boas práticas

- Faça commits pequenos e objetivos.
- Escreva mensagens claras.
- Evite juntar várias alterações diferentes em um único commit.
- Faça commits com frequência.

---

## Commits semânticos

Uma convenção bastante utilizada é o **Conventional Commits**.

Estrutura:

```
tipo(escopo): descrição
```

Exemplos:

```text
feat(login): adiciona autenticação com JWT

fix(api): corrige validação de CPF

docs(commit): adiciona documentação sobre commits

refactor(user): reorganiza serviço de usuários

test(auth): adiciona testes unitários

chore: atualiza dependências
```

---

## Tipos mais comuns

| Tipo | Utilização |
|-------|------------|
| feat | Nova funcionalidade |
| fix | Correção de bug |
| docs | Documentação |
| style | Ajustes de formatação |
| refactor | Refatoração de código |
| test | Testes |
| chore | Manutenção do projeto |
| perf | Melhorias de desempenho |
| ci | Configuração de integração contínua |

---

## Resumo

O commit é a principal forma de registrar alterações em um projeto Git. Um histórico organizado, com commits pequenos e mensagens descritivas, facilita a colaboração entre desenvolvedores e a manutenção do código.

---

## Próximo tópico

➡️ [04 - Branch](04-branch.md)