# Pacumê · Pavê da Farofinha

Landing page da Pacumê: o clássico Pavê da Farofinha em copinhos individuais, entregue congelado em São Paulo.

Site estático (HTML + CSS, sem build). Funciona direto no GitHub Pages.

## Estrutura

```
index.html            página completa (textos, estilos e script)
assets/img/           logo, ilustrações e foto do carrinho
.nojekyll             faz o GitHub Pages servir os arquivos sem processar
```

## Publicar no GitHub Pages

1. Crie um repositório (ex.: `pacume-site`) e suba todos os arquivos desta pasta, mantendo a estrutura.
2. No repositório: **Settings → Pages**.
3. Em **Source**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`, e salve.
4. Em 1–2 minutos o site fica no ar em `https://SEU-USUARIO.github.io/pacume-site/`.

## Conectar um domínio próprio (quando tiver)

1. Em **Settings → Pages → Custom domain**, digite o domínio (ex.: `www.pacume.com.br`) e salve. O GitHub cria um arquivo `CNAME` no repositório.
2. No painel do registro do domínio (Registro.br, GoDaddy etc.), crie os DNS:
   - `www` → registro **CNAME** apontando para `SEU-USUARIO.github.io`
   - domínio raiz (`pacume.com.br`) → quatro registros **A**:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
3. Depois que o DNS propagar, marque **Enforce HTTPS**.
4. Atualize a tag `og:image` no `index.html` para a URL completa (ex.: `https://www.pacume.com.br/assets/img/og-image.jpg`), para a prévia aparecer certinha no WhatsApp e redes sociais.

## Onde editar

Tudo está no `index.html`:

| O que | Onde procurar |
|---|---|
| Número do WhatsApp e mensagem pronta | bloco `<script>` no fim do arquivo (`WHATSAPP` e `DEFAULT_MSG`) |
| Preços (individual, kit com 4, pavê grande de 750 ml) | seção `id="funcionamento"`, classe `tier` |
| Aviso de frete e retirada em Pinheiros | classe `frete` |
| Itens, preços e mensagem do "Monte o seu pedido" | bloco `<script>` no fim do arquivo (`ITEMS` e a montagem de `msg`) |
| Texto de eventos e legenda do carrinho | seção `id="eventos"` |
| E-mail, Instagram, entrega e retirada | seção `id="contato"` |
| Cores e fontes | bloco `:root` no início do `<style>` |

Fontes (Google Fonts): **Playfair Display** itálico (títulos), **Amatic SC** (etiquetas escritas à mão) e **Karla** (texto).
