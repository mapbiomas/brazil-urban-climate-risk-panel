# Painel Risco Climático e Urbano — MapBiomas

**Site:** https://mapbiomas.github.io/brazil-urban-climate-risk-panel/
**Repositório:** https://github.com/mapbiomas/brazil-urban-climate-risk-panel

Página única (`index.html`), sem build nem servidor: ao abrir, ela lê os arquivos JSON da pasta `data/`
e monta o painel no navegador. Fonte: **MapBiomas Risco Climático, Coleção 11** (série 1985–2025).

## O que o painel mostra

- **Temas:** suscetibilidade a **inundação** e a **deslizamento** da área urbana (classes Médio, Alto e Muito alto),
  **Módulo Urbano** (área urbanizada não vegetada, áreas verdes urbanas e vegetação periurbana, vegetação intraurbana)
  e **Luz Noturna** (2013–2025).
- **Recortes:** Brasil, estados, municípios e favelas (Luz Noturna não tem dado por favela).
- **Rankings de 2025** e série histórica de cada território.
- Os números indicam **suscetibilidade** da área urbana, não dano nem ocorrência de desastre. Valores em hectares (1 km² = 100 ha).

## Estrutura

```
index.html            página do painel
data/index.json       lista de territórios (Brasil, UFs, municípios, favelas) e metadados (anos, fonte)
data/agregados.json   séries agregadas
data/favrec.json      recortes de favelas
data/mun_<UF>.json    dados dos municípios de cada UF (carregado só quando a UF é aberta)
data/fav_<UF>.json    dados das favelas de cada UF
.nojekyll             faz o GitHub Pages publicar os arquivos como estão
```

## Publicação (GitHub Pages)

Uma vez, em **Settings → Pages → Build and deployment**: *Deploy from a branch*, branch `main`, pasta `/ (root)` → **Save**.
Em alguns minutos o site fica no endereço acima (acompanhe em **Actions → pages build and deployment**).

## Atualizar os dados

Substitua os arquivos de `data/` (mesmos nomes e mesmo formato) e faça commit na `main`.
O site atualiza em alguns minutos; se aparecer a versão antiga, recarregue com Ctrl+Shift+R.
