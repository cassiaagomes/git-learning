# Prática 02 - Simulando e resolvendo um conflito de merge

## Objetivo

Simular um conflito de merge e documentar o passo a passo para resolver.

Essa prática usa duas branches alterando a mesma linha de um arquivo. Assim, o Git não consegue escolher sozinho qual versão manter e pede uma resolução manual.

---

## Cenário da simulação

Vamos criar um arquivo simples com uma frase sobre Git.

Depois, duas branches diferentes vão alterar a mesma frase:

- A branch `docs/conflito-versao-a` vai escrever uma versão da frase.
- A branch `docs/conflito-versao-b` vai escrever outra versão da mesma frase.

Quando tentarmos juntar as duas alterações na `main`, o Git vai gerar um conflito.

---

## Passo 1 - Criar arquivo base

Primeiro, vá para a branch principal:

```bash
git switch main
```

Crie um arquivo chamado `praticas/frase-conflito.md` com o conteúdo:

```md
# Frase para conflito

Git ajuda no controle de versões.
```

Adicione e faça o commit do arquivo base:

```bash
git add praticas/frase-conflito.md
git commit -m "docs: adiciona arquivo base para conflito"
```

Esse commit representa o ponto inicial da simulação.

---

## Passo 2 - Criar primeira branch

Crie a primeira branch:

```bash
git switch -c docs/conflito-versao-a
```

Altere a frase para:

```md
Git ajuda equipes a controlar versões de projetos.
```

Depois registre essa alteração:

```bash
git add praticas/frase-conflito.md
git commit -m "docs: altera frase pela versao a"
```

Nesse momento, a branch `docs/conflito-versao-a` tem uma alteração própria.

---

## Passo 3 - Voltar para main e criar segunda branch

Volte para a `main`:

```bash
git switch main
```

Crie a segunda branch:

```bash
git switch -c docs/conflito-versao-b
```

Altere a mesma frase para:

```md
Git permite registrar e recuperar versões de um projeto.
```

Depois registre essa alteração:

```bash
git add praticas/frase-conflito.md
git commit -m "docs: altera frase pela versao b"
```

Agora existem duas branches com alterações diferentes na mesma linha do mesmo arquivo.

---

## Passo 4 - Integrar a primeira branch na main

Volte para a branch `main`:

```bash
git switch main
```

Faça o merge da primeira branch:

```bash
git merge docs/conflito-versao-a
```

Esse merge deve funcionar normalmente, porque a `main` ainda não tinha outra alteração conflitante nessa linha.

Depois desse merge, o arquivo fica assim:

```md
# Frase para conflito

Git ajuda equipes a controlar versões de projetos.
```

---

## Passo 5 - Tentar integrar a segunda branch

Agora tente fazer o merge da segunda branch:

```bash
git merge docs/conflito-versao-b
```

O Git deve indicar um conflito, porque as duas branches alteraram a mesma linha.

Uma mensagem parecida com esta pode aparecer:

```text
Auto-merging praticas/frase-conflito.md
CONFLICT (content): Merge conflict in praticas/frase-conflito.md
Automatic merge failed; fix conflicts and then commit the result.
```

---

## Passo 6 - Ver arquivos em conflito

```bash
git status
```

O Git deve mostrar o arquivo `praticas/frase-conflito.md` como conflitante.

Exemplo de saída:

```text
both modified: praticas/frase-conflito.md
```

---

## Passo 7 - Entender os marcadores do conflito

Abra o arquivo `praticas/frase-conflito.md`.

Ele deve estar parecido com:

```text
<<<<<<< HEAD
Git ajuda equipes a controlar versões de projetos.
=======
Git permite registrar e recuperar versões de um projeto.
>>>>>>> docs/conflito-versao-b
```

Esses marcadores significam:

| Marcador | Significado |
| --- | --- |
| `<<<<<<< HEAD` | Início da versão que está na branch atual, neste caso a `main` |
| `=======` | Separação entre as duas versões |
| `>>>>>>> docs/conflito-versao-b` | Fim da versão que veio da branch que está sendo integrada |

---

## Passo 8 - Resolver manualmente

Para resolver, escolha uma das versões ou combine as duas.

Neste exemplo, vamos combinar as duas ideias em uma frase final:

```md
# Frase para conflito

Git ajuda equipes a controlar, registrar e recuperar versões de um projeto.
```

O arquivo final não pode ter os marcadores:

```text
<<<<<<<
=======
>>>>>>>
```

Depois de resolver, salve o arquivo.

---

## Passo 9 - Registrar a resolução

Adicione o arquivo resolvido:

```bash
git add praticas/frase-conflito.md
```

Finalize o merge criando o commit de resolução:

```bash
git commit -m "fix: resolve conflito na frase de exemplo"
```

Também é possível usar uma mensagem mais descritiva:

```bash
git commit -m "docs: resolve conflito de merge documentado"
```

---

## Passo 10 - Conferir histórico

```bash
git log --oneline --graph --all
```

Esse comando ajuda a visualizar as branches e o commit de resolução.

Exemplo do que deve aparecer no histórico:

```text
*   a1b2c3d docs: resolve conflito de merge documentado
|\
| * e4f5g6h docs: altera frase pela versao b
* | i7j8k9l docs: altera frase pela versao a
|/
* m1n2o3p docs: adiciona arquivo base para conflito
```

---

## Resultado esperado

Ao final, o arquivo `praticas/frase-conflito.md` deve conter apenas a versão resolvida:

```md
# Frase para conflito

Git ajuda equipes a controlar, registrar e recuperar versões de um projeto.
```

O merge estará concluído e o conflito terá sido resolvido manualmente.

---

## Resumo do que aconteceu

1. Criamos um arquivo base na `main`.
2. Criamos duas branches a partir da mesma base.
3. Cada branch alterou a mesma linha do arquivo.
4. Fizemos merge da primeira branch sem problema.
5. Ao tentar fazer merge da segunda branch, o Git encontrou conflito.
6. Abrimos o arquivo, removemos os marcadores e escrevemos a versão final.
7. Fizemos um commit registrando a resolução do conflito.

---

## Checklist da prática

- [ ] Arquivo base criado.
- [ ] Branch A criada e alterada.
- [ ] Branch B criada e alterada.
- [ ] Primeiro merge realizado.
- [ ] Conflito gerado no segundo merge.
- [ ] Conflito resolvido manualmente.
- [ ] Commit de resolução criado.
- [ ] Histórico conferido.
