# Conflitos de merge

## O que é um conflito de merge?

Um conflito de merge acontece quando o Git não consegue decidir automaticamente qual alteração deve ser mantida.

Isso geralmente ocorre quando duas branches modificam a mesma linha ou a mesma região de um arquivo.

---

## Exemplo de conflito

Imagine que a branch `main` tem esta linha:

```text
Git é uma ferramenta de versionamento.
```

Uma branch altera para:

```text
Git é uma ferramenta de controle de versão.
```

Outra branch altera para:

```text
Git é um sistema distribuído de controle de versão.
```

Quando essas alterações forem integradas, o Git pode gerar um conflito.

---

## Como o conflito aparece no arquivo

O Git marca o conflito assim:

```text
<<<<<<< HEAD
Git é uma ferramenta de controle de versão.
=======
Git é um sistema distribuído de controle de versão.
>>>>>>> docs/conflito
```

Significado:

- `<<<<<<< HEAD`: versão da branch atual;
- `=======`: separação entre as versões;
- `>>>>>>> nome-da-branch`: versão da branch que está sendo integrada.

---

## Como resolver

1. Abra o arquivo com conflito.
2. Escolha qual versão manter ou combine as duas.
3. Apague os marcadores `<<<<<<<`, `=======` e `>>>>>>>`.
4. Salve o arquivo.
5. Adicione o arquivo resolvido.
6. Faça o commit da resolução.

Exemplo:

```bash
git status
git add docs/arquivo-com-conflito.md
git commit -m "fix: resolve conflito de merge"
```

---

## Abortando um merge

Se quiser cancelar o merge antes de resolver:

```bash
git merge --abort
```

Use com cuidado, pois isso descarta a tentativa de merge em andamento.

---

## Dicas para evitar conflitos

- Atualize sua branch com frequência.
- Faça commits pequenos.
- Evite muitas pessoas editando a mesma parte do arquivo ao mesmo tempo.
- Abra Pull Requests menores.
- Comunique mudanças grandes para a equipe.

---

## Resumo

Conflitos fazem parte do trabalho com Git. O importante é entender os marcadores, escolher a versão correta, remover os marcadores e registrar a resolução em um commit.

---

## Próximo tópico

[10 - Boas práticas](10-boas-praticas.md)
