# Valheim · Itens To-Do

Lista de coleta/progressão para **Valheim**, num único arquivo HTML auto-contido.
Abrir o `index.html` no navegador já funciona — sem build, sem backend, sem dependências externas.

## O que tem

- **1230 itens** em 10 categorias: `Ammo`, `Armor`, `Building`, `Food`, `Material`,
  `Misc`, `Tool`, `Trinket`, `Trophy`, `Weapon`.
- Cada item traz nome, categoria, **bioma** (`b`), **local de craft** (`s`) e a
  **receita** (`cost`).
- Marcador de concluído (todo/done) com barra de progresso no topo.
- Estado salvo em `localStorage` (chave `valheim-todo-v2`), então seu progresso
  fica no navegador mesmo fechando a página.

## Estrutura

```
index.html      app inteiro (dados + lógica + estilo num arquivo só)
icons/          ícones dos itens (.png)
```

- `index.html` é o app completo; os dados dos itens vivem dentro dele.
- `icons/<nome>.png` são os ícones; se um ícone não existir a UI mostra um
  glifo da categoria como fallback.

## Como usar

```bash
# opção 1: abrir direto
start index.html

# opção 2: servir localmente (evita quinhões de CORS, se precisar)
python -m http.server 8000
# -> http://localhost:8000
```

## Créditos

Nomes de itens, categorias e receitas obtidos de dados abertos da comunidade
Valheim (ValheimSaveParser). Ícones servidos do CDN do valheim.tools.
