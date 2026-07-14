# Exemplo de .gitignore

O arquivo `.gitignore` informa ao Git quais arquivos ou pastas não devem ser versionados.

Exemplo:

```gitignore
# Dependencias
node_modules/
vendor/

# Arquivos de ambiente
.env
.env.local

# Logs
*.log

# Builds
dist/
build/

# Sistema operacional
.DS_Store
Thumbs.db

# Editores
.vscode/
.idea/
```

## Quando usar

Use `.gitignore` para evitar enviar arquivos que:

- São gerados automaticamente;
- Contêm informações sensíveis;
- São específicos da sua máquina;
- Não fazem parte do código ou da documentação do projeto.
