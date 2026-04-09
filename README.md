# backend-clientes

Aplicação desenvolvida em JavaScript com Node.js e Express.

## Requisitos

Antes de começar, é necessário ter instalado no computador:

- Git
- Node.js

## Versão do Node

Este projeto foi desenvolvido com Node 20.

Recomenda-se utilizar essa mesma versão para evitar diferenças de comportamento entre ambientes.

## Como clonar o projeto

No terminal, execute:

```bash
git clone https://github.com/developercorrea-dev/backend-clientes.git
cd backend-clientes
```

## Como instalar as dependências

Após clonar o projeto, execute:

```bash
npm ci
```

Esse comando instala as dependências exatamente conforme definido no `package-lock.json`, deixando o ambiente mais padronizado entre diferentes computadores.

## Caso ocorra erro no npm ci

Se houver algum problema de consistência entre `package.json` e `package-lock.json`, execute:

```bash
npm install
```

## Como executar o projeto

Se o projeto estiver configurado para execução padrão, use:

```bash
npm start
```

Se estiver configurado com script de desenvolvimento, use:

```bash
npm run dev
```

## Fluxo completo para os alunos

```bash
git clone https://github.com/developercorrea-dev/backend-clientes.git
cd backend-clientes
npm ci
npm start
```

Se o `npm ci` apresentar erro, tentar:

```bash
npm install
npm start
```

## Como publicar no GitHub do aluno

Depois de clonar o projeto do professor, o aluno pode enviar o projeto para um repositório no GitHub dele.

### Passo 1: criar um repositório vazio no GitHub do aluno

No GitHub do aluno, criar um novo repositório vazio.

Exemplo:

- Nome do repositório: `backend-clientes`
- Não adicionar README
- Não adicionar `.gitignore`
- Não adicionar licença

### Passo 2: verificar o remoto atual

Após o clone, o repositório estará apontando para o GitHub do professor.

```bash
git remote -v
```

### Passo 3: trocar o endereço do remoto para o GitHub do aluno

Substituir a URL abaixo pela URL do repositório criado pelo aluno.

```bash
git remote set-url origin https://github.com/joaoenascimento9/backend-clientes.git
```

### Passo 4: confirmar o novo remoto

```bash
git remote -v
```

Agora o `origin` deve apontar para o GitHub do aluno.

### Passo 5: enviar o projeto para o GitHub do aluno

```bash
git push -u origin main
```

## Alternativa: manter o repositório do professor como referência

Se o aluno quiser manter o repositório do professor como referência para futuras atualizações, pode fazer assim:

### Renomear o remoto atual do professor para `upstream`

```bash
git remote rename origin upstream
```

### Adicionar o GitHub do aluno como novo `origin`

```bash
git remote add origin https://github.com/USUARIO-DO-ALUNO/backend-clientes.git
```

### Conferir os remotos

```bash
git remote -v
```

Exemplo esperado:

```bash
origin   https://github.com/USUARIO-DO-ALUNO/backend-clientes.git (fetch)
origin   https://github.com/USUARIO-DO-ALUNO/backend-clientes.git (push)
upstream https://github.com/developercorrea-dev/backend-clientes.git (fetch)
upstream https://github.com/developercorrea-dev/backend-clientes.git (push)
```

### Enviar para o GitHub do aluno

```bash
git push -u origin main
```

### Atualizar com mudanças do professor no futuro

```bash
git pull upstream main
```

## Estrutura básica do projeto

- `package.json` → define o projeto e suas dependências
- `package-lock.json` → trava as versões instaladas
- `node_modules` → pasta gerada automaticamente com as dependências
- `.gitignore` → define arquivos e pastas que não devem subir para o GitHub

## Observações importantes

### 1. A pasta `node_modules` não vai para o GitHub

A pasta `node_modules` é criada localmente após a instalação das dependências. Por isso, ela não deve ser enviada ao repositório.

### 2. Após clonar, é necessário instalar as dependências

Mesmo com o projeto clonado, as dependências não vêm junto. Por isso, é obrigatório executar:

```bash
npm ci
```

ou, se necessário:

```bash
npm install
```

### 3. Não é necessário instalar o Express separadamente

Não é preciso executar:

```bash
npm install express
```

pois o Express já faz parte das dependências do projeto, desde que ele esteja corretamente listado no `package.json`.

### 4. O arquivo `package-lock.json` deve permanecer no repositório

Ele ajuda a manter as mesmas versões de dependências para todos que clonarem o projeto.

## Atualizando o projeto local

Se houver novas alterações no GitHub, execute:

```bash
git pull
```

## Possíveis erros comuns

### `npm` não é reconhecido

Isso indica que o Node.js não foi instalado corretamente ou não está no PATH do Windows.

### Erro ao instalar dependências

Tente primeiro:

```bash
npm ci
```

Se não funcionar:

```bash
npm install
```

### Erro de versão do Node

Preferencialmente, utilize Node 20.

## Autor

Projeto disponibilizado para fins de estudo e prática em sala de aula.
