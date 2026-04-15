# CLAUDE.md — E-COMMERCEGUIDE

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** E-COMMERCEGUIDE
**Nicho:** Negócios e Empreendedorismo
**Keywords:** Ola Meu nome e Roberto sou uma pessoa do bem com o
**Paleta de cores:** slate | **Fonte:** outfit

Ola! Meu nome é Roberto, sou uma pessoa do bem com o objetivo de ajudar as pessoas que buscam conhecimento e aprimoramento no nosso mercado. Eu trabalho na área há 10 anos na área e para mim é um prazer poder compartilhar conhecimento através da internet. Já estou há 1 ano trabalhando duro para o crescimento do blog e acredito muito que seremos o blog mais visitado do nosso mercado. O conteúdo do blog é direcionado ao público iniciante no assunto. Não espere técnicas e estratégias avançadas por aqui. Aqui você vai encontrar diversos reviews e análises técnicas sobre diversos assunto dentro do mercado. Todas as análises são feitas por especialistas e eu dedico muito tempo nas pesquisas antes de publicar.



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-D |
| Hero | Hero-B |
| Features | Features-G |
| About Section | About-G |
| Posts | Posts-H |
| Footer | Footer-E |
| Página Sobre | Sobre-B |
| Página Contato | Contato-I |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
