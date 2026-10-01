# 🍺 Empório Cervisia — Site de Demonstração

Página única (*single-page*) de demonstração para o **Empório Cervisia**, bar e restaurante em Jaú-SP, com cardápio interativo, horários, mapa e atalhos para WhatsApp e delivery.

> ⚠️ **Aviso:** este é um projeto de demonstração, feito sem compromisso. **Não é o site oficial** do estabelecimento e não está divulgado. A página já inclui `noindex, nofollow`, então não aparece em buscadores.

---

## 📋 Sobre o projeto

O objetivo é mostrar como um site simples, rápido e bonito pode ajudar um bar/restaurante local a:

- apresentar o ambiente e os pratos mais pedidos;
- exibir o cardápio completo de forma organizada, por categorias;
- informar horários (com destaque para o **dia de hoje**), endereço e formas de pagamento;
- levar o cliente ao pedido em **um toque** (WhatsApp ou delivery).

## ✨ Funcionalidades

| Recurso | Descrição |
|---|---|
| **Cardápio interativo** | Abas por categoria (Porções, Hambúrgueres, Sanduíches, Pratos principais, Massas, Risotos, Individuais, Kids, Saladas, Bebidas e sobremesa), geradas por JavaScript a partir de um objeto `MENU` |
| **Selos nos pratos** | "★ Destaque" e "Vegetariano" |
| **Horário do dia** | Detecta o dia da semana com `new Date()` e destaca a linha de hoje na tabela |
| **Navegação fixa** | Menu *sticky* com rolagem suave e versão mobile (botão ☰) |
| **Animação ao rolar** | Elementos aparecem com `IntersectionObserver` (respeita `prefers-reduced-motion`) |
| **Galeria de fotos** | Grade responsiva com 4 fotos do ambiente |
| **Mapa** | Google Maps incorporado via `iframe` |
| **Botão flutuante** | WhatsApp sempre visível no canto da tela |
| **Responsivo** | Layout adaptado para celular, tablet e desktop |

## 🧱 Estrutura da página

1. **Faixa de aviso** de demonstração
2. **Navegação** (Destaques · Ambiente · Cardápio · Música · Como chegar)
3. **Hero** com logo, chamada e botões (cardápio, WhatsApp, delivery)
4. **Barra de informações rápidas** (horário de hoje, endereço, delivery)
5. **Destaques** (3 cards)
6. **Ambiente** (galeria)
7. **Cardápio** (abas + lista)
8. **Música** (identidade da casa)
9. **Como chegar** (horários, contato, pagamento, mapa)
10. **Avaliações** (Google e TripAdvisor)
11. **Rodapé** (redes sociais e crédito)

## 🛠️ Tecnologias

- **HTML5** semântico
- **CSS3** puro: variáveis (`:root`), Grid, Flexbox, `clamp()`, `position: sticky`, *media queries*
- **JavaScript** puro (*vanilla*), sem frameworks nem bibliotecas
- **Google Fonts:** Oswald, DM Sans e Caveat
- Imagens **embutidas em Base64** dentro do próprio HTML

## 🚀 Como executar

Não precisa instalar nada.

1. Baixe o arquivo `emporio-cervisia-demo.html`.
2. Dê dois cliques para abrir no navegador.

Ou, se preferir rodar um servidor local (bom para praticar):

```bash
# na pasta do projeto
python3 -m http.server 8000
# depois acesse http://localhost:8000/emporio-cervisia-demo.html
```

> 💡 Para as fontes do Google e o mapa funcionarem, é necessário estar **conectado à internet**.

## ✏️ Como personalizar

**Cardápio** — edite o objeto `MENU` no `<script>`. Cada item segue o formato:

```js
["Nome do prato", "Descrição", preço, "Selo opcional"]
// exemplo:
["A Mais Pedida", "Batata frita com catupiry...", 45, "Top"]   // "Top" = Destaque, "Veg" = Vegetariano
```

**Horários** — edite o array `H` no `<script>` (um item por dia da semana, começando no domingo).

**Cores** — altere as variáveis no início do CSS:

```css
:root{
  --vinho:#6b0a0a;  --ouro:#d4a24c;  --creme:#f5ebdd;  /* ... */
}
```

**Textos e links** — WhatsApp, e-mail, delivery, Instagram, Facebook e avaliações estão em tags `<a href="...">` no HTML.

**Crédito do rodapé** — troque o texto `[SEU NOME] · [SEU WHATSAPP]` pelos seus dados antes de mostrar o projeto a alguém.

## ⚠️ Pontos de atenção

- **Tamanho do arquivo:** por causa das imagens em Base64, o HTML tem cerca de **2,9 MB**. Para uma versão de produção, o ideal é separar as imagens em arquivos (`/img`) e otimizá-las (WebP).
- **Direitos de imagem:** logo, fotos e nome pertencem ao estabelecimento. Antes de publicar ou divulgar, **peça autorização** ao proprietário.
- **Dados do cardápio:** os preços foram tirados do cardápio de delivery e podem variar no salão. Sempre confirme com o estabelecimento.
- **Acessibilidade:** vale melhorar o texto alternativo (`alt`) das imagens e testar o contraste das cores.

## 🔮 Ideias de melhorias

- [ ] Separar em `index.html`, `style.css` e `script.js`
- [ ] Mover o cardápio para um arquivo `menu.json`
- [ ] Converter imagens para WebP e usar `loading="lazy"`
- [ ] Adicionar modo "Aberto agora / Fechado" em tempo real
- [ ] Publicar no GitHub Pages ou Netlify
- [ ] Adicionar uma versão em inglês

## 📄 Licença

Defina a licença do código (por exemplo, MIT). Textos, imagens e marca pertencem ao Empório Cervisia.

## 👤 Autor

Demonstração desenvolvida por **[SEU NOME]** · [SEU WHATSAPP]

---

## 🇺🇸 English summary

A single-page **demo website** for *Empório Cervisia*, a bar and restaurant in Jaú, Brazil. It features an interactive menu with category tabs, opening hours that highlight today, an embedded map, and quick links to WhatsApp and delivery. Built with plain **HTML, CSS and JavaScript** (no frameworks). This is an unofficial demo and is not affiliated with the business.

**Run it:** just open `emporio-cervisia-demo.html` in your browser.
