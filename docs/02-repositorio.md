# Repositório Git

## O que é um repositório?

Um repositório (repository ou simplesmente *repo*) é o local onde o Git armazena todos os arquivos de um projeto, juntamente com o histórico completo de alterações realizadas ao longo do desenvolvimento.

Além dos arquivos do projeto, o repositório registra informações como:

- Histórico de commits;
- Branches;
- Tags;
- Autor de cada alteração;
- Data e horário das modificações.

Essas informações permitem acompanhar a evolução do projeto e recuperar versões anteriores sempre que necessário.

---

## Tipos de repositório

### Repositório Local

É o repositório armazenado no computador do desenvolvedor.

Todas as alterações, commits e branches podem ser criadas localmente, mesmo sem conexão com a internet.

Exemplo de criação:

```bash
git init
```

---

### Repositório Remoto

É uma cópia do projeto hospedada em um servidor, permitindo colaboração entre vários desenvolvedores.

Plataformas populares para hospedagem de repositórios Git incluem:

- GitHub
- GitLab
- Bitbucket
- Azure DevOps

O repositório remoto é utilizado para compartilhar código, realizar revisões, abrir Pull Requests e integrar alterações da equipe.

---

## Estrutura de um repositório Git

Quando um diretório é inicializado com Git, é criada uma pasta oculta chamada:

```
.git
```

Essa pasta contém todas as informações necessárias para o funcionamento do Git, como:

- Histórico de commits;
- Configurações do repositório;
- Objetos do Git;
- Referências para branches e tags.

Por esse motivo, a pasta `.git` não deve ser modificada manualmente.

---

## Criando um repositório

Para criar um novo repositório Git, basta executar:

```bash
git init
```

Após esse comando, o diretório passa a ser monitorado pelo Git.

---

## Clonando um repositório existente

Caso o projeto já exista em um servidor remoto, utilize:

```bash
git clone <url-do-repositorio>
```

Exemplo:

```bash
git clone https://github.com/usuario/projeto.git
```

Esse comando cria uma cópia completa do projeto no computador, incluindo todo o histórico de commits.

---

## Boas práticas

- Utilize nomes claros para os repositórios.
- Mantenha um arquivo `README.md` atualizado.
- Utilize um arquivo `.gitignore` para evitar versionar arquivos desnecessários.
- Faça commits frequentes e organizados.
- Utilize branches para desenvolver novas funcionalidades.

---

## Resumo

O repositório é a base de qualquer projeto controlado pelo Git. É nele que ficam armazenados o código-fonte, o histórico de alterações e todas as informações necessárias para o controle de versões e a colaboração entre desenvolvedores.

---

## Próximo tópico

➡️ [03 - Commit](03-commit.md)