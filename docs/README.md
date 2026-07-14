# Git Learning

Repositório pessoal de estudos sobre Git e GitHub, criado para registrar anotações, comandos, práticas e exemplos da trilha de versionamento.

## Objetivos

- Entender os conceitos principais do Git.
- Praticar comandos básicos do dia a dia.
- Trabalhar com branches.
- Demonstrar o fluxo completo de Pull Request / Merge Request.
- Simular e resolver conflitos de merge.
- Registrar boas práticas de commits, organização e colaboração.

## Conteúdo

### Conceitos e comandos

1. [O que é Git](docs/01-o-que-e-git.md)
2. [Repositório Git](docs/02-repositorio.md)
3. [Commit](docs/03-commit.md)
4. [Branch](docs/04-branch.md)
5. [Merge](docs/05-merge.md)
6. [Remote](docs/06-remote.md)
7. [Comandos básicos](docs/07-comandos-basicos.md)
8. [Pull Request e Merge Request](docs/08-pull-request-merge-request.md)
9. [Conflitos de merge](docs/09-conflitos-de-merge.md)
10. [Boas práticas](docs/10-boas-praticas.md)

### Práticas guiadas

- [Fluxo completo: branch, commits, PR e merge](praticas/01-fluxo-completo-branch-pr-merge.md)
- [Simulação e resolução de conflito de merge](praticas/02-simulando-resolvendo-conflito.md)
- [Checklist de comandos para revisão](praticas/03-checklist-comandos.md)

### Exemplos

- [Mensagens de commit](exemplos/mensagens-commit.md)
- [Modelo de Pull Request](exemplos/modelo-pull-request.md)
- [Exemplo de .gitignore](exemplos/gitignore-exemplo.md)

## Fluxo de estudo sugerido

1. Ler os arquivos da pasta `docs` em ordem.
2. Reproduzir as práticas da pasta `praticas`.
3. Usar os arquivos de `exemplos` como referência.
4. Criar commits pequenos para cada novo tópico estudado.
5. Abrir Pull Requests para praticar o fluxo colaborativo.

## Comandos mais usados

```bash
git clone <url>
git status
git add .
git commit -m "docs: descreve a alteracao"
git push
git pull
git fetch
git branch
git switch -c minha-branch
git merge minha-branch
```

## Status da trilha

- [x] Repositório pessoal criado.
- [x] Anotações iniciais sobre Git, repositório e commit.
- [x] Documentação sobre branch, merge e remote.
- [x] Documentação dos comandos básicos.
- [x] Fluxo de Pull Request / Merge Request.
- [x] Simulação de conflito de merge.
- [x] Boas práticas de versionamento.
