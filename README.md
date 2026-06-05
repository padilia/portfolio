# Lucas Padilia — GitHub Pages

Portfólio estático pronto para publicação no GitHub Pages.

## Estrutura

```text
.
├── index.html
├── 404.html
├── .nojekyll
├── css/
│   └── style.css
├── js/
│   └── main.js
└── images/
```

## Publicação no GitHub Pages

1. Crie um repositório, por exemplo `lucaspadilia.github.io`.
2. Envie todos os arquivos deste pacote para a branch `main`.
3. No GitHub, acesse **Settings > Pages**.
4. Em **Build and deployment**, selecione:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/root`
5. Salve e aguarde a publicação.

## Foto automática do LinkedIn

A área principal usa o badge público do LinkedIn:

```html
<script src="https://platform.linkedin.com/badges/js/profile.js" async defer type="text/javascript"></script>
```

Esse badge é renderizado pelo próprio LinkedIn com `data-vanity="lucaspadilia"`. Quando a foto pública do LinkedIn for alterada, o badge tende a refletir a mudança automaticamente.

Para funcionar corretamente, no LinkedIn a foto precisa estar pública em **Public profile settings > Profile Photo**. Caso o LinkedIn bloqueie o carregamento do badge por política, extensão de navegador, privacidade ou alteração da própria plataforma, o site continua funcional com o link para o perfil.

## Segurança aplicada

- Sem backend e sem formulário de envio.
- Sem coleta de dados do visitante.
- Links externos com `rel="noopener noreferrer"`.
- Meta `referrer` com `strict-origin-when-cross-origin`.
- Política CSP em meta tag permitindo apenas recursos próprios e o badge do LinkedIn.
- Arquivo `.nojekyll` para evitar processamento desnecessário no GitHub Pages.

## Customização rápida

- Conteúdo principal: `index.html`
- Identidade visual: `css/style.css`
- Comportamentos simples: `js/main.js`
- Imagens: `images/`
