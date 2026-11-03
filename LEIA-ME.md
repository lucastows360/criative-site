# Site — Criative Comunicação Visual

Site estático (HTML, CSS e JavaScript), sem etapa de build. Animações com GSAP 3.12.5 + ScrollTrigger (carregados por CDN).

## Estrutura

```
index.html        página única com todas as seções
css/style.css     estilos (cores e fontes no bloco :root do topo)
js/main.js        menu, galeria, lightbox, formulário, mapa e animações
img/              fotos dos trabalhos + og-image.jpg (imagem de compartilhamento)
```

## Testar no computador

Abra o `index.html` no navegador. Para testar como no servidor:

```
cd criative
python -m http.server 8000
```
e acesse http://localhost:8000

## Publicar no GitHub Pages

1. Crie um repositório chamado `criative` na conta `lucastows360`.
2. Envie todo o conteúdo desta pasta (index.html, css, js, img) para a raiz do repositório.
3. Em Settings → Pages, escolha a branch `main` e a pasta `/ (root)`.
4. O site fica em https://lucastows360.github.io/criative/

Se usar outro nome de repositório ou um domínio próprio, troque o endereço nas tags `canonical`, `og:url`, `og:image` e no JSON-LD do `index.html` (busque por `lucastows360.github.io/criative`).

## Adicionar fotos ao portfólio

1. Salve a foto em `img/` (JPG, idealmente até 1600 px de largura).
2. Em `js/main.js`, acrescente uma linha na lista `PROJETOS`:

```js
{ src: "img/nome-da-foto.jpg", titulo: "Nome do cliente", cat: "fachadas" },
```

Categorias: `fachadas`, `letras`, `envelopamento`, `adesivos`, `banners`. Os filtros e contadores se atualizam sozinhos.

As fotos atuais foram recortadas dos prints do Instagram e têm resolução limitada. Substitua pelos arquivos originais mantendo o mesmo nome para melhorar a nitidez.

## Contatos configurados

- WhatsApp (botões gerais): https://wa.me/message/IQM5HS4LX3RFI1
- WhatsApp com mensagem pronta (formulário e botões dos serviços): 55 43 99648-7663 — variável `WA_NUMERO` no topo do `js/main.js`
- Instagram: https://www.instagram.com/criative_design1107/
- Endereço: Avenida Minas Gerais, 2186, Apucarana – PR, 86812-285

O mapa do Google é carregado automaticamente quando o site está publicado.
