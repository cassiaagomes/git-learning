# Comandos básicos

Este arquivo reúne os comandos mais usados no dia a dia com Git.

---

## `git clone`

Cria uma cópia local de um repositório remoto.

```bash
git clone https://github.com/usuario/projeto.git
```

Use quando o projeto já existe no GitHub e você quer trabalhar nele no seu computador.

---

## `git status`

Mostra o estado atual dos arquivos.

```bash
git status
```

Ajuda a verificar:

- Arquivos modificados;
- Arquivos novos;
- Arquivos preparados para commit;
- Branch atual.

---

## `git add`

Adiciona alterações à Staging Area.

```bash
git add arquivo.md
```

Adicionar tudo:

```bash
git add .
```

---

## `git commit`

Registra as alterações no histórico do Git.

```bash
git commit -m "docs: adiciona anotacoes sobre git"
```

---

## `git push`

Envia commits locais para o repositório remoto.

```bash
git push
```

Primeiro push de uma branch nova:

```bash
git push -u origin nome-da-branch
```

---

## `git pull`

Baixa alterações do repositório remoto e tenta integrá-las à branch atual.

```bash
git pull
```

Equivale, de forma simplificada, a buscar alterações e aplicar na branch local.

---

## `git fetch`

Busca informações do repositório remoto, mas não aplica automaticamente na branch atual.

```bash
git fetch
```

Use quando quiser conferir o que mudou no remoto antes de atualizar sua branch.

---

## Diferença entre `pull` e `fetch`

| Comando | O que faz |
| --- | --- |
| `git fetch` | Baixa referências do remoto, mas não altera seus arquivos automaticamente |
| `git pull` | Baixa alterações e tenta integrar na branch atual |

---

## Sequência comum de trabalho

```bash
git status
git switch -c docs/novo-topico
git add .
git commit -m "docs: adiciona novo topico"
git push -u origin docs/novo-topico
```

---

## Resumo rápido

| Comando | Uso |
| --- | --- |
| `git clone` | Copiar um repositório remoto |
| `git status` | Verificar estado dos arquivos |
| `git add` | Preparar alterações |
| `git commit` | Registrar alterações |
| `git push` | Enviar commits |
| `git pull` | Baixar e integrar alterações |
| `git fetch` | Baixar referências sem integrar |

---

## Próximo tópico

[08 - Pull Request e Merge Request](08-pull-request-merge-request.md)
