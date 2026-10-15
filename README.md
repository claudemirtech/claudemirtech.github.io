# claudemirtech.github.io

Esta é a página principal do meu site.

## Subprojetos

* base64
* unicode
* contador

## Deploy no GitHub Pages

Orientações para publicação de acordo com o tipo de projeto:

### 1. Projeto HTML Simples

Quando o projeto for HTML simples:

* Utilizar o workflow do GitHub Actions: `.github/workflows/static.yml`.
* Configurações do repositório no GitHub:
  1. Acesse as configurações do repositório (**Settings**).
  2. No menu lateral esquerdo, selecione **Pages**.
  3. Na seção **Build and deployment**, altere o campo **Source** para **GitHub Actions**.

### 2. Projeto React + Vite

Quando o projeto for React + Vite:

#### Instalar o Vite

```bash
npm install -g vite
```

#### Criar o projeto

```bash
npm create vite@latest
```

#### Instalar dependências

```bash
npm install
npm run dev
```

#### Configuração do GitHub Pages

Instale o pacote `gh-pages`:

```bash
npm install gh-pages
```

No seu arquivo `vite.config.js`, inclua a propriedade `base` com o nome do seu repositório:

```javascript
base: '/example'
```

No seu arquivo `package.json`, inclua o campo `homepage` com a URL do seu repositório:

```json
"homepage": "https://<username>.github.io/<repository>"
```

No seu `package.json`, inclua os dois scripts:

```json
"predeploy": "npm run build",
"deploy": "gh-pages -d dist"
```

#### Executar o deploy

```bash
npm run deploy
```
