# Prática 03 - Checklist de comandos

Use esta lista para revisar os principais comandos da trilha.

## Preparação

```bash
git status
git branch
git remote -v
```

- [ ] Conferi a branch atual.
- [ ] Conferi se existem alterações pendentes.
- [ ] Conferi se o remote está configurado.

---

## Criar branch

```bash
git switch -c docs/minha-pratica
```

- [ ] Criei uma branch com nome claro.

---

## Registrar alterações

```bash
git status
git add .
git diff --staged
git commit -m "docs: adiciona pratica de comandos"
```

- [ ] Verifiquei os arquivos alterados.
- [ ] Adicionei apenas o necessário.
- [ ] Revisei o que será commitado.
- [ ] Escrevi uma mensagem clara.

---

## Enviar para o remoto

```bash
git push -u origin docs/minha-pratica
```

- [ ] Enviei a branch para o GitHub.
- [ ] Abri um Pull Request.

---

## Atualizar local depois do merge

```bash
git switch main
git pull
git branch -d docs/minha-pratica
```

- [ ] Voltei para a branch principal.
- [ ] Atualizei o repositório local.
- [ ] Removi a branch local finalizada.

---

## Revisão rápida

| Situação | Comando |
| --- | --- |
| Ver alterações | `git status` |
| Preparar arquivo | `git add arquivo` |
| Criar commit | `git commit -m "mensagem"` |
| Criar branch | `git switch -c nome` |
| Trocar branch | `git switch nome` |
| Enviar commits | `git push` |
| Buscar alterações | `git fetch` |
| Baixar e integrar | `git pull` |
| Juntar branches | `git merge nome` |
